---
title: "Testquiz"
description: 
date: 2024-01-24T15:41:52Z
image: 
math: 
license: 
comments: true
draft: false
---

<div id="quiz">
  <h2>Quiz Title</h2>
  <div id="question-container">
    <p id="question">Question goes here?</p>
  </div>
  <div id="options-container">
    <button onclick="checkAnswer('option1')">Option 1</button>
    <button onclick="checkAnswer('option2')">Option 2</button>
    <!-- Add more options as needed -->
  </div>
  <p id="result"></p>
</div>

<script>
  // JavaScript code for the quiz
  let currentQuestion = 0;
  let score = 0;

  const quizData = [
    {
      question: "Question 1?",
      options: {
        option1: "Answer 1",
        option2: "Answer 2",
        // Add more options as needed
      },
      correctAnswer: "option1",
    },
    // Add more questions as needed
  ];

  function loadQuestion() {
    const questionContainer = document.getElementById("question");
    const optionsContainer = document.getElementById("options-container");

    questionContainer.textContent = quizData[currentQuestion].question;

    optionsContainer.innerHTML = "";
    for (const option in quizData[currentQuestion].options) {
      const button = document.createElement("button");
      button.textContent = quizData[currentQuestion].options[option];
      button.onclick = function () {
        checkAnswer(option);
      };
      optionsContainer.appendChild(button);
    }
  }

  function checkAnswer(selectedOption) {
    if (selectedOption === quizData[currentQuestion].correctAnswer) {
      score++;
    }

    currentQuestion++;

    if (currentQuestion < quizData.length) {
      loadQuestion();
    } else {
      displayResult();
    }
  }

  function displayResult() {
    const resultContainer = document.getElementById("result");
    resultContainer.textContent = `Your score: ${score} out of ${quizData.length}`;
  }

  // Load the first question
  loadQuestion();
</script>
