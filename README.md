# umimecesky-solver
╰ Javascript code to solve https://umimecesky.cz for you <br>

**Initial code from https://github.com/MiftikCZ/umimecesky-solver**
<br> <br>

**⚠Not finished⚠**

# Code:
```
function answer() {
  var correct_answer = -1
   try {
      var answers = questions.find(q => q.id == window.location.pathname.split("/")[2])
      for (i in answers.options.length) {parseInt(Value, radix)
         if (answers.options[i].correct === 1)
            correct_answer = i
      }
      console.log("Correct answer: " + correct_answer + 1)
   } catch (error) {}
}

answer()
```
