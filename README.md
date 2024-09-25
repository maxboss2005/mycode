<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CorelDRAW Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 170vh;
            margin: 0;
        }
        .quiz-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            width: 3000px;
            text-align: left;
        }
        .question {
            font-weight: bold;
        }
        .answer {
            margin: 5px 0;
        }
        #submit {
            margin-top: 10px;
            padding: 5px 10px;
            cursor: pointer;
        }
        #result {
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <div id="quiz">
    

<p class="question">1. What is CorelDRAW primarily used for?</p>
<div class="answer">
    <input type="radio" name="q1" value="a"> Word processing<br>
    <input type="radio" name="q1" value="b"> Vector graphic design<br>
    <input type="radio" name="q1" value="c"> Video editing
</div>

<p class="question">2. Which file format is native to CorelDRAW?</p>
<div class="answer">
    <input type="radio" name="q2" value="a"> .cdr<br>
    <input type="radio" name="q2" value="b"> .psd<br>
    <input type="radio" name="q2" value="c"> .ai
</div>

<p class="question">3. Which tool in CorelDRAW is used to draw freehand lines?</p>
<div class="answer">
    <input type="radio" name="q3" value="a"> Pen Tool<br>
    <input type="radio" name="q3" value="b"> Bezier Tool<br>
    <input type="radio" name="q3" value="c"> Freehand Tool
</div>

<p class="question">4. Which feature allows you to combine two or more objects into one in CorelDRAW?</p>
<div class="answer">
    <input type="radio" name="q4" value="a"> Group<br>
    <input type="radio" name="q4" value="b"> Weld<br>
    <input type="radio" name="q4" value="c"> Combine
</div>

<p class="question">5. What is the shortcut key to 'Undo' an action in CorelDRAW?</p>
<div class="answer">
    <input type="radio" name="q5" value="a"> Ctrl + U<br>
    <input type="radio" name="q5" value="b"> Ctrl + Z<br>
    <input type="radio" name="q5" value="c"> Ctrl + Y
</div>

<p class="question">6. Which tool is used to create text in CorelDRAW?</p>
<div class="answer">
    <input type="radio" name="q6" value="a"> Text Tool<br>
    <input type="radio" name="q6" value="b"> Shape Tool<br>
    <input type="radio" name="q6" value="c"> Zoom Tool
</div>

<p class="question">7. What is the maximum number of pages you can add to a CorelDRAW document?</p>
<div class="answer">
    <input type="radio" name="q7" value="a"> 50<br>
    <input type="radio" name="q7" value="b"> Unlimited<br>
    <input type="radio" name="q7" value="c"> 100
</div>

<p class="question">8. Which of the following is used to add effects like shadows and glows in CorelDRAW?</p>
<div class="answer">
    <input type="radio" name="q8" value="a"> Effects Menu<br>
    <input type="radio" name="q8" value="b"> Arrange Menu<br>
    <input type="radio" name="q8" value="c"> File Menu
</div>

<p class="question">9. Which tool is used to adjust the shape of objects in CorelDRAW?</p>
<div class="answer">
    <input type="radio" name="q9" value="a"> Pick Tool<br>
    <input type="radio" name="q9" value="b"> Shape Tool<br>
    <input type="radio" name="q9" value="c"> Eyedropper Tool
</div>

<p class="question">10. Which option allows you to save your CorelDRAW file as a template?</p>
<div class="answer">
    <input type="radio" name="q10" value="a"> Save As<br>
    <input type="radio" name="q10" value="b"> Export<br>
    <input type="radio" name="q10" value="c"> Save as Template
</div>

<button id="submit">Submit</button>
            <div id="result"></div>
        </div>
    </div>
    

    <script>
       document.getElementById('submit').onclick = function() {
    let score = 0;
    let resultText = "";


    // Correct answers
    const correctAnswers = {
        q1: 'b',
        q2: 'a',
        q3: 'c',
        q4: 'c',
        q5: 'b',
        q6: 'a',
        q7: 'b',
        q8: 'a',
        q9: 'b',
        q10: 'c'
    };

    // Check answers
    for (let question in correctAnswers) {
        const selectedAnswer = document.querySelector(`input[name="${question}"]:checked`);
        
        if (selectedAnswer && selectedAnswer.value === correctAnswers[question]) {
            score++;
            resultText += `Question ${question.slice(1)}: Correct!<br>`;
        } else {
            resultText += `Question ${question.slice(1)}: Incorrect. The correct answer is: ${correctAnswers[question]}<br>`;
        }
    }

    // Display result
    document.getElementById('result').innerHTML = `You scored ${score} out of 10.<br><br>${resultText}`;};
    </script>
