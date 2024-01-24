---
title: "Testquiz"
description: 
date: 2024-01-24T16:20:58Z
image: 
math: 
license: 
comments: true
draft: false
---
# Quiz Time!

## Question 1
What is the capital of France?

- [ ] Berlin
- [ ] Madrid
- [x] Paris
- [ ] Rome

## Question 2
Which planet is known as the Red Planet?

- [ ] Earth
- [ ] Mars
- [ ] Jupiter
- [x] Venus

<script>
  // Add event listener for checkbox clicks
  document.addEventListener('click', function(event) {
    if (event.target.type === 'checkbox') {
      checkAnswer(event.target);
    }
  });

  // Function to check the answer and provide feedback
  function checkAnswer(checkbox) {
    var question = checkbox.closest('h2').textContent.trim();
    var answerText = checkbox.parentElement.textContent.trim();
    var explanation = '';

    if (question === 'Question 1') {
      if (checkbox.checked) {
        // Correct answer
        checkbox.parentElement.style.backgroundColor = 'lightgreen';
        explanation = 'The correct answer is Paris. Did you know that before its French name, the city was called "Parisius" when it was part of the Western Roman Empire?';
      } else {
        // Incorrect answer
        checkbox.parentElement.style.backgroundColor = 'lightcoral';
        explanation = 'Incorrect. The correct answer is Paris. Did you know that before its French name, the city was called "Parisius" when it was part of the Western Roman Empire?';
      }
    } else if (question === 'Question 2') {
      if (checkbox.checked) {
        // Correct answer
        checkbox.parentElement.style.backgroundColor = 'lightgreen';
        explanation = 'The correct answer is Venus. Fun fact: Venus is often referred to as the "Evening Star" or the "Morning Star" depending on its appearance in the sky.';
      } else {
        // Incorrect answer
        checkbox.parentElement.style.backgroundColor = 'lightcoral';
        explanation = 'Incorrect. The correct answer is Venus. Fun fact: Venus is often referred to as the "Evening Star" or the "Morning Star" depending on its appearance in the sky.';
      }
    }

    // Add explanation text below the answers
    var explanationElement = document.createElement('p');
    explanationElement.textContent = explanation;
    checkbox.parentElement.parentNode.appendChild(explanationElement);
  }
</script>
