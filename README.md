# travel-site
HTML, CSS, JavaScript를 활용한 여행지 소개 웹 페이지입니다.
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>브라질 여행 소개</title>
<style>
  body { background: #d9f0e6; font-family: "맑은 고딕", sans-serif; margin: 20px; color: #333; }
  h1 { color: #3b7a57; }
  .section { background: #f0fbf7; border-radius: 15px; padding: 15px; margin: 10px 0; }
  button { background: #a3d9a5; border: none; padding: 10px 15px; border-radius: 10px; cursor: pointer; }
</style>
</head>
<body>
  <h1>브라질 여행에 오신 것을 환영합니다!</h1>

  <div class="section">
    <h2>주요 관광지</h2>
    <p>코파카바나 해변, 이과수 폭포, 리우데자네이루의 예수 그리스도상</p>
    <button onclick="alert('코파카바나 해변은 세계적으로 유명한 해변입니다!')">코파카바나 해변 소개</button>
  </div>

  <div class="section">
    <h2>브라질 음식</h2>
    <p>페이조아다, 아사이볼 같이 맛있는 음식들이 많아요.</p>
    <button onclick="alert('페이조아다는 콩과 고기로 만든 전통 음식입니다.')">페이조아다 설명</button>
  </div>
</body>
</html>
