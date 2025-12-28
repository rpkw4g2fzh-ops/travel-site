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
    background: #e2f3f5;
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
    border-radius: 12px;
    object-fit: cover;
  }
  .place h3 {
    margin: 10px 0 5px;
    color: #2a5d7e;
  }
  .place p {
    font-size: 0.95rem;
    color: #555;
  }

  /* 음식 소개 */
  .foods {
    text-align: center;
  }
  .food-item {
    margin: 15px 0;
  }
  button.food-btn {
    background-color: #9fe2bf;
    border: none;
    border-radius: 15px;
    padding: 12px 22px;
    font-size: 1rem;
    cursor: pointer;
    box-shadow: 1px 3px 6px #7dbf9e;
    transition: background-color 0.3s ease;
  }
  button.food-btn:hover {
    background-color: #7fc6a6;
    color: #fff;
  }
  .food-desc {
    margin-top: 10px;
    color: #3b5a40;
    font-size: 1rem;
    display: none;
  }

  /* 이미지 슬라이더 */
  .slider {
    position: relative;
    max-width: 100%;
    margin: 0 auto 40px;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 2px 2px 15px #a9c7bc;
  }
  .slides {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }
  .slides img {
    width: 100%;
    border-radius: 20px;
    object-fit: cover;
  }
  .slider-btn {
    position: absolute;
    top: 45%;
    font-size: 2rem;
    background: rgba(255,255,255,0.7);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    width: 40px; height: 40px;
    line-height: 37px;
    text-align: center;
    user-select: none;
  }
  .prev-btn {
    left: 15px;
  }
  .next-btn {
    right: 15px;
  }
  .slider-btn:hover {
    background: #69a2b0;
    color: white;
  }
  /* 반응형 */
  @media (max-width: 700px) {
    .places {
      flex-direction: column;
      align-items: center;
    }
    .place {
      flex: none;
      width: 90%;
    }
  }

  footer {
    text-align: center;
    font-size: 0.9rem;
    color: #7a7a7a;
    padding: 15px 0;
    border-top: 1px solid #ddd;
    margin-top: 30px;
  }

</style>
</head>
<body>

<header>
  <h1>브라질 여행으로 떠나요!</h1>
</header>

<main>

  <section>
    <h2>여행지 사진 슬라이더</h2>
    <div class="slider">
      <div class="slides" id="slides">
        <img src="https://cdn.pixabay.com/photo/2017/06/20/23/01/brazil-2425518_1280.jpg" alt="브라질 풍경1" />
        <img src="https://cdn.pixabay.com/photo/2020/03/12/18/31/brazil-4920080_1280.jpg" alt="코파카바나 해변" />
        <img src="https://cdn.pixabay.com/photo/2016/08/13/06/29/statue-of-christ-1599825_1280.jpg" alt="예수 그리스도 상" />
      </div>
      <button class="slider-btn prev-btn" onclick="prevSlide()">&#10094;</button>
      <button class="slider-btn next-btn" onclick="nextSlide()">&#10095;</button>
    </div>
  </section>

  <section>
    <h2>주요 관광지</h2>
    <div class="places">
      <div class="place" onclick="showPopup('코파카바나 해변은 세계적으로 유명한 해변으로, 맑은 바다와 아름다운 모래사장이 펼쳐져 있습니다.')">
        <img src="https://cdn.pixabay.com/photo/2015/03/26/09/41/brazil-690293_1280.jpg" alt="코파카
