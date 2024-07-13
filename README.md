<!DOCTYPE html>
<html>
<head>
  <title>노인 일자리 추천 앱</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background-color: #f5f5f5;
    }

    h1 {
      color: #333;
    }

    form {
      margin-bottom: 20px;
    }

    label, select {
      display: block;
      margin: 10px 0;
    }

    button {
      margin-top: 10px;
      padding: 10px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

    #recommendations {
      margin-top: 20px;
      font-size: 1.2em;
    }
  </style>
</head>
<body>
  <h1>노인 일자리 추천</h1>
  <form id="recommendationForm">
    <label for="age">나이:</label>
    <select id="age" name="age">
      <option value="1">0~19세</option>
      <option value="2">20~39세</option>
      <option value="3">40~64세</option>
      <option value="4">65~79세</option>
      <option value="5">80세 이상</option>
    </select><br>
    
    <label for="education">교육 수준:</label>
    <select id="education" name="education">
      <option value="1">초등학교 졸업</option>
      <option value="2">중학교 졸업</option>
      <option value="3">고등학교 졸업</option>
      <option value="4">대학교 학사 졸업</option>
      <option value="5">대학교 석사 졸업</option>
      <option value="6">대학교 박사 이상 졸업</option>
    </select><br>
    
    <label for="interest">관심 분야:</label>
    <select id="interest" name="interest">
      <option value="1">다른 사람의 욕구나 복지에 관련된 직업군</option>
      <option value="2">상대방을 설득해 거래를 성사시키는 직업군</option>
      <option value="3">기업이나 단체 조직에 효율적인 운영에 관련된 직업군</option>
      <option value="4">상품과 재화의 생산, 유지, 운송을 비롯해 정보통신, 공학, 기능, 기계 무역에 관한 직업군</option>
      <option value="5">농수산, 축산, 지하자원, 천연자원 등을 개발, 보존, 수확하는 직업군</option>
      <option value="6">과학 이론 연구 및 그 이론을 환경에 적용하는 직업군</option>
      <option value="7">예술과 연예에 관련된 직업군</option>
      <option value="8">교육, 언론, 법률 등 문화유산의 보존, 전수에 관련된 직업군</option>
    </select><br>
    
    <button type="button" onclick="getRecommendation()">추천받기</button>
  </form>
  <div id="recommendations"></div>

  <script>
    function getRecommendation() {
      var age = document.getElementById('age').value;
      var education = document.getElementById('education').value;
      var interest = document.getElementById('interest').value;

      var recommendations = "";

      if (interest == "1" && education == "4" && age == "4") {
        recommendations = "사회복지사, 보육교사, 은행 창구 직원, 경비원, 여행 가이드, 항공 승무원, 피트니스 트레이너, 이벤트 코디네이터, 주차 관리원, 아파트 관리사무소 직원";
      } else if (interest == "2") {
        recommendations = "경영 컨설턴트, 마케팅 매니저, 금융 분석가, 인사 관리자, 판매 관리자, 공공 관계 전문가, 회계사, 상품 기획자, 광고 기획자, 보험 설계사";
      } else if (interest == "3") {
        recommendations = "경찰관, 소방관, 군인, 공무원, 법원 직원, 교사, 보건소 직원, 환경 감시관, 구청 직원, 세무 공무원";
      } else if (interest == "4") {
        recommendations = "소프트웨어 개발자, 데이터 분석가, 네트워크 관리자, 시스템 관리자, 웹 개발자, 전기 기술자, 전자 기술자, 기계 공학자, 로봇 공학자, 항공 기술자";
      } else if (interest == "5") {
        recommendations = "농부, 어부, 산림 관리원, 환경 보호 활동가, 건설 노동자, 도로공사 작업자, 야생동물 보호원, 스포츠 코치, 레인저, 해양 연구원";
      } else if (interest == "6") {
        recommendations = "물리학자, 화학자, 생물학자, 천문학자, 기상학자, 지질학자, 해양학자, 생명과학자, 환경 과학자, 약학 연구원";
      } else if (interest == "7") {
        recommendations = "배우, 가수, 무용가, 음악가, 화가, 작가, 연출가, 영화감독, 방송 진행자, 성우";
      } else if (interest == "8") {
        recommendations = "도서관 사서, 박물관 큐레이터, 문화재 전문가, 출판 편집자, 문예 창작자, 문화 기획자, 영화 평론가, 문학 평론가, 서적 판매자, 전시 기획자";
      } else {
        recommendations = "다른 관심 분야를 선택해주세요.";
      }

      document.getElementById('recommendations').innerText = "추천 직업: " + recommendations;
    }
  </script>
</body>
</html>
