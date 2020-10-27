---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Python Puzzle
---
# Python Review

## Discount t-shirts
Re-arrange the blocks below so they ask the user how many t-shirts they want to purchase.
100 or fewer t-shirts: 5% discount
200 or fewer t-shirts: 10% discount
500 or fewer t-shirts: 15% discount
More than 500 t-shirts: 20% discount
Display the discount.

<div id="discount-t-shirt-sortableTrash" class="sortable-code"></div> 
<div id="discount-t-shirt-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="discount-t-shirt-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="discount-t-shirt-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "quantity = int(input('How many t-shirts will you purchase?'))\n" +
    "if quantity <= 100:\n" +
    "	discount = quantity * 0.05\n" +
    "elif quantity <= 200:\n" +
    "	discount = quantity * 0.1\n" +
    "elif quantity <= 500:\n" +
    "	discount = quantity * 0.15\n" +
    "else:\n" +
    "	discount = quantity * 0.2\n" +
    "print('Your discount is', discount, '%')\n" +
    "elif: #distractor\n" +
    "else discount > 500: #distractor\n" +
    "quantity * 0.15 = discount #distractor\n" +
    "if discount == 0.05: #distractor\n" +
    "print('Your discount', 'discount') #distractor\n" +
    "quantity = input('How many t-shirts will you purchase?') #distractor\n" +
    "input = ('How many t-shirts will you purchase?') #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "discount-t-shirt-sortable",
    "max_wrong_lines": 3,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "discount-t-shirt-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#discount-t-shirt-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#discount-t-shirt-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
