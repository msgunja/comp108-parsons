---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Sequencing code
---
# Parsons Practice

## Parsons 1  
Re-arrange the blocks below: this assigns the name 'Sarah' to a variable, and prints statements in logical order.
<div id="parsons-1-sortableTrash" class="sortable-code"></div> 
<div id="parsons-1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="parsons-1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="parsons-1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "name = &quot;Sarah&quot;\n" +
    "print(&quot;Hello there!&quot;)\n" +
    "print(&quot;Welcome to programming, &quot; + name)\n" +
    "print(&quot;Have a great day!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "parsons-1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#parsons-1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#parsons-1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
