<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>편견 진단 테스트</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #f9f9f9;
      color: #333;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #0078d4;
      color: white;
      padding: 20px;
    }
    main {
      padding: 20px;
      max-width: 800px;
      margin: 0 auto;
    }
    .question {
      display: none;
      margin: 20px 0;
    }
    .question.active {
      display: block;
    }
    .choice {
      display: block;
      background-color: #ffa500;
      color: white;
      border: none;
      padding: 15px;
      margin: 10px auto;
      width: 80%;
      font-size: 1rem;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .choice:hover {
      background-color: #e59400;
    }
    #result {
      margin-top: 30px;
      font-size: 1.4rem;
      color: #0078d4;
    }
  </style>
</head>
<body>
  <header>
    <h1>편견 진단 테스트</h1>
    <p>모든 질문에 답한 후, 결과를 확인하세요!</p>
  </header>
  <main>
    <div id="quiz">
      <!-- 질문 1 -->
      <div class="question active" data-type="방어적 편견">
        <p>1. 다른 사람들이 내 전공에 부정적인 이야기를 할 때, 그것이 나를 공격한다고 느낀 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('방어적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 2 -->
      <div class="question" data-type="소외적 편견">
        <p>2. 특정 그룹의 사람들과 이야기할 때, 그들이 나와 다르다는 느낌이 들었던 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('소외적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 3 -->
      <div class="question" data-type="합리화 편견">
        <p>3. 친구의 실수가 있을 때, "그 사람도 힘든 상황이었을 거야."라고 스스로 위로한 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('합리화 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 4 -->
      <div class="question" data-type="방어적 편견">
        <p>4. 친구들이 내 취미를 비웃을 때, 그들이 나를 진심으로 이해하지 못한다고 생각한 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('방어적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 5 -->
      <div class="question" data-type="소외적 편견">
        <p>5. 동아리에서 특정 사람을 피하고 싶다는 생각이 들었던 순간이 있었나요?</p>
        <button class="choice" onclick="recordAnswer('소외적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 6 -->
      <div class="question" data-type="합리화 편견">
        <p>6. 다른 사람의 잘못된 선택에 대해 "나는 그럴 상황이라면 그렇게 했을 것 같아."라고 생각한 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('합리화 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 7 -->
      <div class="question" data-type="방어적 편견">
        <p>7. 자신의 선택에 대해 다른 사람들이 의문을 제기했을 때, 그들이 내 결정을 무시한다고 느낀 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('방어적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 8 -->
      <div class="question" data-type="소외적 편견">
        <p>8. 수업 중 특정 친구들이 나와 어울리지 않는다고 느낀 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('소외적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 9 -->
      <div class="question" data-type="합리화 편견">
        <p>9. 누군가의 행동이 이해가 안 갈 때, 그 이유를 찾으려 하지 않고 그냥 넘긴 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('합리화 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 10 -->
      <div class="question" data-type="방어적 편견">
        <p>10. 의견이 다를 때, 상대방을 설득하려는 마음이 강했던 경험이 있나요?</p>
        <button class="choice" onclick="recordAnswer('방어적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 11 -->
      <div class="question" data-type="소외적 편견">
        <p>11. 다른 문화적 배경을 가진 사람들과 소통할 때, 그들이 나를 이해하지 못한다고 생각한 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('소외적 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
      <!-- 질문 12 -->
      <div class="question" data-type="합리화 편견">
        <p>12. 특정 상황에서 누군가의 결정을 비판하면서도, "그럴 수밖에 없었겠다."고 느낀 적이 있나요?</p>
        <button class="choice" onclick="recordAnswer('합리화 편견')">예</button>
        <button class="choice" onclick="recordAnswer()">아니요</button>
      </div>
    </div>

    <div id="result" style="display: none;">
      <h2>결과</h2>
      <p id="resultText"></p>
    </div>
  </main>

  <script>
    const answers = {
      "방어적 편견": 0,
      "소외적 편견": 0,
      "합리화 편견": 0
    };
    let currentQuestionIndex = 0;
    const questions = document.querySelectorAll(".question");

    function recordAnswer(type) {
      // 답변 기록
      if (type) {
        answers[type]++;
      }

      // 현재 질문 숨기기
      questions[currentQuestionIndex].classList.remove("active");
      currentQuestionIndex++;

      // 다음 질문 표시
      if (currentQuestionIndex < questions.length) {
        questions[currentQuestionIndex].classList.add("active");
      } else {
        showResult();
      }
    }

    function showResult() {
      const resultDiv = document.getElementById("result");
      const resultText = document.getElementById("resultText");
      const highest = Object.keys(answers).reduce((a, b) =>
        answers[a] > answers[b] ? a : b
      );
      resultText.innerText = `당신은 ${highest} 성향이 강한 편입니다.`;
      resultDiv.style.display = "block";
    }
  </script>
</body>
</html>
