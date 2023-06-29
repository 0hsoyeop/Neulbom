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
### 1. 메인화면 ⬇️
- header, 갤러리, footer로 이루어져있다.
- 메인 화면의 '로그인' 버튼을 클릭하여 로그인 페이지로 이동한다.
- 로그인은 '직원, 입주자, 보호자'로 구분하여 처리한다.

- **늘봄 소개** : 인사말, 시설소개, 오시는길
- **입주안내**
- **알림게시판** : 공지사항, 식단표, 생활게시판
- **커뮤니티** : 입주상담, 문의게시판, 자유게시판
![1-1  메인화면](https://github.com/0hsoyeop/TW-Library/assets/131536077/c10348ee-cc0e-4dae-bfa0-250f585164f3)
![1-2  메인화면](https://github.com/0hsoyeop/TW-Library/assets/131536077/fbc9bff8-0659-4104-aa4f-8306c0f9c0df)
![1-3  메인화면](https://github.com/0hsoyeop/TW-Library/assets/131536077/32504c99-6fe2-4d9e-8894-bad4b00790f2)

### 2. 게시판 ⬇️
- 비회원은 입주상담 글을 등록, 조회, 수정, 삭제할 수 있다. 
- 비회원이 글을 작성하려면 이름과 전화번호를 입력받는다.
- **입력받은 정보와 일치하는 글만 조회** 할 수 있다.
- 문의글에 관리자가 답변을 등록하고, 해당 글에는 **[답변완료]** 표시를 한다.
![4-1  비회원 입주상담](https://github.com/0hsoyeop/TW-Library/assets/131536077/12d9e993-7ce5-4cb7-b6c1-aaac2b033c86)

### 3. 관리자 - 재무관리 ⬇️
- chart.js를 사용하여 DB의 데이터와 연동된 차트를 출력한다.
- **원형차트** : 실버타운 입주자, 요양원 입주자 수를 표시
- **라인차트** : 최근 5개월 간의 지출 총액을 표시
- **최근지출내역** : 최근 10건의 지출 항목과 금액 등, 총 지출액 표시 
![3  재무관리](https://github.com/0hsoyeop/TW-Library/assets/131536077/9fc98612-c5a1-4078-a735-4b691446c4b2)

---
### 담당 업무 상세보기
### 최근 지출 내역 조회
- 사용된 테이블: 지출내역 (tblSpend)

<table>
    <tr>
    <th>지출내역 (tblSpend)</th>
    </tr>
    <tr>
        <td>지출번호</td>
    </tr>
    <tr>
        <td>지출항목</td>
    </tr>
    <tr>
        <td>카테고리</td>
    </tr>
    <tr>
        <td>지출금액</td>
    </tr>
    <tr>
        <td>지출날짜</td>
    </tr>
</table>

 ### 🧩 코드 보기
- MoneyDAO.java
- **데이터 베이스에 저장된 지출 내역을 불러와야 하므로 DB select 작업** 을 한다.
- 지출테이블에서 지출날짜, 지출 항목, 카테고리, 지출금액 컬럼을 출력한다.
- 날짜 내림차순 정렬한 **상위 10개 데이터만 불러오기 위해서 rownum으로 범위를 지정** 한다.
- 이때 사용되는 SpendDTO.java의 **SpendDTO는 지출 내역 테이블의 컬럼 정보를 가지고 있다.**
 
```java
	public List<SpendDTO> getLatestSpend() {

		List<SpendDTO> latestSpendList = new ArrayList<SpendDTO>();
		
		try {			
			String sql = "select rownum, a.* from (select to_char(sdate, 'yyyy-mm-dd') as sdate, title, category,
to_char(money, 'FM9,999,999') || '원' as money from tblSpend order by sdate desc) a where rownum <=10";
			
			stat = conn.createStatement();
			rs = stat.executeQuery(sql);
			
			while(rs.next()) {
				SpendDTO spendDto = new SpendDTO();			
				spendDto.setRownum(rs.getInt("rownum"));
				spendDto.setSdate(rs.getString("sdate"));
				spendDto.setTitle(rs.getString("title"));
				spendDto.setCategory(rs.getString("category"));
				spendDto.setMoney(rs.getString("money"));
				
				latestSpendList.add(spendDto);
			}
			
			return latestSpendList;
			
		} catch (Exception e) {
			e.printStackTrace();
		}
		
		return latestSpendList;
	}
```

- **manageMoney.jsp**
	- DAO에서 select하여 얻은 결과를 jsp 페이지로 출력한다.
	- **SpendDTO 객체로부터 지출 내역과 관련된 데이터를 꺼내 jsp에서 사용한다.**

```html
            <table id="latestSpendList-table" class="table table-hover">
           	<colgroup>
					<col width=10%>
					<col width=20%>
					<col width=25%>
					<col width=25%>
					<col width=20%>
			</colgroup>
			<thead>
				<tr>
					<th>번호</th>
					<th>날짜</th>
					<th>지출항목</th>
					<th>지출금액</th>
					<th>분류</th>
				</tr>
			<tbody>
				<c:forEach items="${latestSpendList}" var="spendDto">
				<tr>
					<td>${spendDto.rownum}</td>
					<td>${spendDto.sdate}</td>
					<td>${spendDto.title}</td>
					<td>${spendDto.money}</td>
					<td>${spendDto.category}</td>
				</tr>
				</c:forEach>
			</tbody>
			<tfoot>
				<tr>
					<td colspan="3" class="latestSpendList-total">합계</td>
					<td class="latestSpendList-total">${spendSum}</td>
					<td></td>
				</tr>
			</tfoot>
			</table>
```

### ⬇️ 웹 페이지에는 이렇게 표시된다! ⬇️
![image](https://github.com/0hsoyeop/Neulbom/assets/131536077/26664855-e618-4272-8922-3d4e03e0cd6c)


--- 
## 개발 스토리
### 회고
<table>
    <tr>
        <td>💡 시행착오가 가장 많았던 프로젝트</td>
    </tr>
</table>


- **프로젝트 팀장이 해야할 일은?** 
  
![image](https://github.com/0hsoyeop/Neulbom/assets/131536077/674615a2-b75c-4654-aecc-5e9b520f0497)

 <p> 웹 프로젝트에서는 팀장을 맡았습니다.  팀원들 모두 서버 구현을 어려워했기 때문에 화면 설계를 짧은 시간 내에 끝내고 
 남은 기간을 백엔드 개발에 몰두할 수 있도록 일정을 세웠습니다. 
 ERD와 더미데이터 담당, 화면설계 담당을 나누어 Figma로 화면을 하나씩 만들어보기 시작했습니다. 그러나 여기서부터 조금씩 일이 꼬이기 시작했습니다.</p>  
 <p>HTML 코드를 추출하기 위해  Figma를 선택하였는데, 팀원들 중 누구도 사용법을 잘 알지 못해 화면 설계에 시간이 많이 소요됐습니다. 
 게다가 Figma로 추출한 코드는 거의 모든 것을 다시 수정해야할 정도로 손이 많이 갔습니다. 생각과는 다른 방향으로 일이 흘러가니, 예상 일정보다 2~3일 정도 늦어지게 되었습니다. </p>
 <p>프로젝트 기간이 길지 않았기 때문에 마음이 초조했습니다. 팀원들과 함께 상의하여 결정한 툴이었지만, 
 팀장으로서 조금 더 알아보고 프로젝트에 적합한 프로그램을 찾아서 개발을 추진했으면 좋았을 것이라는 아쉬움이 들었습니다. </p>  


   - **개발의 목표를 생각하자** 
  <p>시간이 부족하다보니 처음 떠올렸던 모든 기능을 구현할 수는 없었습니다. 회원과 관리자의 채팅 , 부트스트랩을 활용해서 UI 요소를 다양하게 구성하는 것, 직원 근태 관리 등등. 이미 팀원들 각자 맡은 업무의 진행도가 더딘 상황이라 이런 부가적인 기능은 후순위로 미뤄야 했습니다.</p>
 <p>구현하지 못하는 업무가 생기자 모두 아쉬워했습니다. 그러나 이번 프로젝트의 가장 주된 목표는 Servlet과 JSP로 페이지를 안정적으로 만들어보는 것이라고 생각했습니다. 그래서 이번에 미처 완성하지 못한 기능은 Spring 프로젝트에서 보완하기로 결정하고, 남은 기간동안 개발에 몰입하여 기한에 맞춰 끝낼 수 있었습니다.</p>  
  <p>개발자로서 정해진 기한을 지키는 것도 중요한 역량이기 때문에, 개발의 목표를 명확히 바로잡고 우선 순위를 잘 생각하여 작업해야 한다는 것을 깨달았습니다.</p>  
