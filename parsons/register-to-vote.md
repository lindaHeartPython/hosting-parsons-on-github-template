<p>Hello-Hello</p>
<div id="register-to-vote-sortableTrash" class="sortable-code"></div> 
<div id="register-to-vote-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="register-to-vote-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="register-to-vote-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "age = int(input('How old are you?'))\n" +
    "if age > = 18:\n" +
    "	print('Register to vote.')\n" +
    "else:\n" +
    "	age = 18 - age\n" +
    "	print('You have to wait', age, 'years')\n" +
    "age = input('How old are you?') #distractor\n" +
    "elif: #distractor\n" +
    "print('age') #distractor\n" +
    "print('You have to wait age years') #distractor\n" +
    "else age < 18: #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "register-to-vote-sortable",
    "max_wrong_lines": 3,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "register-to-vote-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#register-to-vote-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#register-to-vote-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
