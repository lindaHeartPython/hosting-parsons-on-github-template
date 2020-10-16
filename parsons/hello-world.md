---
layout: default
title: Hello World
---
<div id="hello-world-sortableTrash" class="sortable-code"></div> 
<div id="hello-world-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="hello-world-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="hello-world-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print('Hello World')";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "hello-world-sortable",
    "max_wrong_lines": 0,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#hello-world-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#hello-world-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
