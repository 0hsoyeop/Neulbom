# Neulbom
## 실버타운 그룹웨어 & 클라이언트 웹 프로젝트
### 주제
Servlet/JSP를 활용한 웹 프로젝트 구현

### 목적
- 효율적인 운영과 관리를 위한 관리자용 그룹웨어와 실버타운 통합 웹 페이지를 구현하고자 함
- 입주자들의 건강, 삶의 질, 사회 참여 등을 증진하기 위한 실버타운과 요양원을 운영하고,  다양한 서비스와 활동을 제공하기 위해 필요한 기능을 구상한다.
### 사용언어 & 사용기술
<img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white" />  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=HTML5&logoColor=white" />  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=CSS3&logoColor=white" />  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black"/> <br>
<img src="https://img.shields.io/badge/Oracle-F80000?style=flat&logo=oracle&logoColor=white"/>  <img src="https://img.shields.io/badge/jQuery-0769AD?style=flat&logo=jquery&logoColor=white"/>  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=bootstrap&logoColor=white"/>   <img src="https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chart.js&logoColor=white"/>

### 개발도구
<img src="https://img.shields.io/badge/Eclipse IDE-2C2255?style=flat&logo=eclipseide&logoColor=white"/>  <img src="https://img.shields.io/badge/Visual Studio Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white"/>  <img src="https://img.shields.io/badge/Tomcat-F8DC75?style=flat&logo=apachetomcat&logoColor=white"/>  <img src="https://img.shields.io/badge/Sourcetree-0052CC?style=flat&logo=sourcetree&logoColor=white"/> 

### 개발환경
<table>
  <tr>
    <td>OS version (platform)</td>
    <td>Windows(10, 11), Mac OS</td>
  </tr>
  <tr>
    <td>Oracle version</td>
    <td>Oracle Database 11g Express Edition Release 11.2.0.2.0</td>
  </tr>
  <tr>
    <td>Development tool</td>
    <td>SQL Developer, Eclipse, VS code</td>
  </tr>
  <tr>
    <td>Server</td>
    <td>Apache Tomcat 8</td>
  </tr>
  <tr>
    <td>ERD tool</td>
    <td>eXERD</td>
  </tr>
  <tr>
    <td>Language</td>
    <td>JAVA, HTML, CSS, JavaScript, SQL</td>
  </tr>
</table>

### 개요
1. 사용자는 관리자, 입주자, 보호자, 비회원으로 구분한다.
2. 관리자 그룹웨어와 입주자/보호자/비회원 클라이언트 페이지를 구분하여 제공한다.
3. 관리자는 계정 관리자, 일반 관리자, 그 외 직원으로 구분하고 권한별로 기능 접근 권한을 다르게 한다.

### 데이터 구조
![늘봄ERD(논리)](https://github.com/0hsoyeop/Neulbom/assets/131536077/f8214fd5-2b72-4153-8e92-b535a5ad38de)

### 담당업무
- 관리자 화면 설계
- 직원 급여 관리
- 재무 관리 
- 비품 관리
- 복지 프로그램 관리

---
### 화면구성
#### 1. 메인화면
![1-1  메인화면](https://github.com/0hsoyeop/TW-Library/assets/131536077/c10348ee-cc0e-4dae-bfa0-250f585164f3)
![1-2  메인화면](https://github.com/0hsoyeop/TW-Library/assets/131536077/fbc9bff8-0659-4104-aa4f-8306c0f9c0df)
![1-3  메인화면](https://github.com/0hsoyeop/TW-Library/assets/131536077/32504c99-6fe2-4d9e-8894-bad4b00790f2)

#### 2. 게시판
![4-1  비회원 입주상담](https://github.com/0hsoyeop/TW-Library/assets/131536077/12d9e993-7ce5-4cb7-b6c1-aaac2b033c86)

#### 3. 관리자 - 재무관리
![3  재무관리](https://github.com/0hsoyeop/TW-Library/assets/131536077/9fc98612-c5a1-4078-a735-4b691446c4b2)

---

### 구현 기능
#### 복지 프로그램 등록
1. '프로그램 등록' 페이지에서 정보를 입력받는다. 프로그램 일자는 기본값으로 시스템 날짜로 자동 설정된다.
2. form 태그로 입력받은 데이터를 ProgramDAO로 전송한다.
3. DB에 추가할 Index를 getProgSeq()로 구하고 해당 seq로 입력받은 데이터를 insert한다.
4. insert 완료되면 목록 보기 페이지로 이동한다.

- registerProgram.jsp
```HTML
		<form method="POST" action="/neulbom/admin/manage/registerProgram.do">

            	<div>제목</div>
				<input type="text" name="title" class="form-control registerProgram-form" placeholder="프로그램 제목을 입력하세요." required maxlength="15">
            	<div>내용</div>
				<textarea name="content" class="form-control registerProgram-form" maxlength="100" required style="resize: none" placeholder="프로그램 내용을 입력하세요."></textarea>
            	<div>프로그램 날짜</div>
				<input type="date" name="prog_date" id="register-date" class="form-control registerProgram-form" required>
            	
            	<div>강의실</div>
				<select id="place" name="place" class="place form-select">
					<option value="늘봄">늘봄</option>
					<option value="광장">광장</option>
					<option value="늘봄 식당">늘봄 식당</option>
					<option value="늘봄문화홀">늘봄문화홀</option>
				</select>
            	<div>정원</div>
				<input type="number" name="people" class="form-control registerProgram-form" min="1" max="100" value="1" required>
				<input class="btn btn-primary" type="submit" value="등록하기">
		</form>
		
```

- ProgramDAO.java
  - DB연결 설정
```java
	private Connection conn;
	private Statement stat;
	private PreparedStatement pstat;
	private ResultSet rs;
```

```java
	// 프로그램 신규 등록하기
	public int registerProgram(ProgramDTO progDto) {
		
		try {
			
			String sql = "insert into tblProgram(prog_seq, title, prog_date, content, place, people) values(?, ?, to_date(?, 'yyyy-mm-dd hh24:mi:ss'), ?, ?, ?)";
			
			pstat = conn.prepareStatement(sql);
			
			pstat.setString(1, progDto.getProg_seq());
			pstat.setString(2, progDto.getTitle());
			pstat.setString(3, progDto.getProg_date());
			pstat.setString(4, progDto.getContent());
			pstat.setString(5, progDto.getPlace());
			pstat.setString(6, progDto.getPeople());
			
			return pstat.executeUpdate();
			
			
		} catch (Exception e) {
			e.printStackTrace();
		}
		
		
		return 0;
	}

	// 프로그램 seq 구하기
	public String getProgSeq() {
		
		try {
			
			String sql = "select max(prog_seq)+1 as prog_seq from tblProgram";

			
			stat = conn.createStatement();
			rs = stat.executeQuery(sql);
			
			if (rs.next()) {
				return rs.getString("prog_seq");
			}
			
		} catch(Exception e) {
			e.printStackTrace();
		}
		
		
		return null;
	}
```

