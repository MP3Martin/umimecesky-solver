# umimecesky-solver
╰ Javascript code to solve https://umimecesky.cz for you <br>

**Initial code from https://github.com/MiftikCZ/umimecesky-solver**
<br> <br>

**⚠Not finished⚠**

# Code:
```js
function range(n,t,o){null==t&&(t=n||0,n=0),o||(o=t<n?-1:1);for(var r=Math.max(Math.ceil((t-n)/o),0),e=Array(r),a=0;a<r;a++,n+=o)e[a]=n;return e}function answer(){var n=-1;try{var t=questions.find((n=>n.id==window.location.pathname.split("/")[2]));for(i of range(parseInt(t.options.length)))1===t.options[i].correct&&(n=i);console.log("Correct answer: "+parseInt(n+1)),document.getElementById("option"+n).click()}catch(n){}}answer();
```

# Uncompressed code:

```js
function range(start, stop, step) {
  if (stop == null) {
    stop = start || 0;
    start = 0;
  }
  if (!step) {
    step = stop < start ? -1 : 1;
  }

  var length = Math.max(Math.ceil((stop - start) / step), 0);
  var range = Array(length);

  for (var idx = 0; idx < length; idx++, start += step) {
    range[idx] = start;
  }

  return range;
}

function answer() {
  var correct_answer = -1
   try {
      var answers = questions.find(q => q.id == window.location.pathname.split("/")[2])
      for (i of range(parseInt(answers.options.length))) {
         if (answers.options[i].correct === 1)
            correct_answer = i
      }
      console.log("Correct answer: "  + parseInt(correct_answer + 1))
      document.getElementById("option" + correct_answer).click()
   } catch (error) {}
}

answer()
```
