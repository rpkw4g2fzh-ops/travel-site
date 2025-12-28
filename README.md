# travel-site
HTML, CSS, JavaScript를 활용한 여행지 소개 웹 페이지입니다.
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>브라질 여행으로 떠나요!</title>
  <style>
    /* 기본 스타일 */
    body {
      font-family: '맑은 고딕', sans-serif;
      background-color: #e2f3f5;
      color: #2f4f4f;
      margin: 0; padding: 0;
    }
    header {
      background-color: #aee1f9;
      padding: 20px;
      text-align: center;
      border-bottom-left-radius: 25px;
      border-bottom-right-radius: 25px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    header h1 {
      margin: 0;
      color: #2a5d7e;
      font-size: 2.8rem;
      font-weight: bold;
    }
    main {
      max-width: 900px;
      margin: 20px auto;
      padding: 0 15px 50px;
    }
    section {
      background: #d5f0e1;
      border-radius: 20px;
      padding: 20px;
      margin-bottom: 25px;
      box-shadow: 1px 1px 8px #b9e1d7;
    }
    h2 {
      color: #32654f;
      text-align: center;
      margin-top: 0;
      font-size: 2rem;
      letter-spacing: 2px;
    }
    p.description {
      text-align: center;
      font-size: 1.1rem;
      line-height: 1.5;
      margin-bottom: 15px;
    }
    /* 관광지 사진과 설명 */
    .places {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      gap: 15px;
    }
    .place {
      background: #ffffffcc;
      border-radius: 15px;
      box-shadow: 2px 2px 10px rgba(100,100,100,0.1);
      flex: 1 1 calc(33% - 20px);
      min-width: 250px;
      cursor: pointer;
      transition: transform 0.2s ease-in-out;
      text-align: center;
      padding: 15px;
    }
    .place:hover {
      transform: scale(1.05);
    }
    .place img {
      width: 100%;
      height: 140px;
     
