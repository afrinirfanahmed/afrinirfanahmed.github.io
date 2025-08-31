<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>SAT English Prep</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; line-height: 1.6; }
    .hero { background: #4A90E2; color: white; padding: 40px 20px; text-align: center; }
    .modules { display: flex; flex-wrap: wrap; justify-content: center; margin: 20px; }
    .module { background: #f7f7f7; border: 1px solid #ddd; border-radius: 8px; width: 200px; margin: 10px; padding: 20px; text-align: center; }
    button { background: #4A90E2; color: white; border: none; border-radius: 4px; padding: 10px 20px; cursor: pointer; }
    .quiz { max-width: 400px; margin: 40px auto; padding: 20px; background: #fff; border: 1px solid #ccc; border-radius: 8px; }
  </style>
</head>
<body>
  <section class="hero">
    <h1>SAT English Preparation</h1>
    <p>Master Reading, Writing & Grammar for top scores</p>
    <button onclick="scrollToModules()">Get Started</button>
  </section>

  <section id="modules" class="modules">
    <div class="module"><h3>Reading</h3><p>Practice reading passages with comprehension questions.</p></div>
    <div class="module"><h3>Writing</h3><p>Analyze arguments, improve clarity and coherence.</p></div>
    <div class="module"><h3>Grammar</h3><p>Brush up on rules for punctuation, syntax, and usage.</p></div>
  </section>

  <section class="quiz">
    <h3>Mini Quiz</h3>
    <p>Which sentence is grammatically correct?</p>
    <label><input type="radio" name="q1" value="A"> A) She and I went to the store.</label><br/>
    <label><input type="radio" name="q1" value="B"> B) Me and her went to the store.</label><br/>
    <button onclick="checkQuiz()">Submit</button>
    <p id="quizResult"></p>
  </section>

  <script>
    function scrollToModules() {
      document.getElementById('modules').scrollIntoView({ behavior: 'smooth' });
    }

    function checkQuiz() {
      const selected = document.querySelector('input[name="q1"]:checked');
      const result = document.getElementById('quizResult');
      if (!selected) {
        result.textContent = 'Please select an option.';
      } else if (selected.value === 'A') {
        result.textContent = 'Correct! Great job.';
      } else {
        result.textContent = 'Oops! That’s not right. Try again.';
      }
    }
  </script>
</body>
</html>
