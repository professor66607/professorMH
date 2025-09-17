**A) jQuery Basic, jQuery Events**



<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>basic j query</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <h1>hello sahil</h1> 

&nbsp;   <button id="bt1">click me</button> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#bt1").click(function(){ 

&nbsp;               $("h1").text("welcome to our page"); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html>





<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>events</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <p id="para">click or hover me</p> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#para").click(function(){ 

&nbsp;               $(this).css("color","green"); 

&nbsp;           }); 

&nbsp;           $("#para").mouseenter(function(){ 

&nbsp;               $(this).css("background","red"); 

&nbsp;           }); 

&nbsp;           $("#para").mouseleave(function(){ 

&nbsp;               $(this).css("background","white"); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html> 





**B) jQuery Selectors, jQuery Hide and Show effects** 

Code: 



<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>selector</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <p class="cl1">this is class selector</p> 

&nbsp;   <p id="id1">this is id selector</p> 

&nbsp;   <p> this is tag selector</p> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $(".cl1").css("color","red"); 

&nbsp;           $("#id1").css("font-size","20px"); 

&nbsp;           $("p").css("font-weight","bold"); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html> 

Output: 

&nbsp;

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>hind and show</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <p id="text1">this is a para</p> 

&nbsp;   <button id="hide">hide button</button> 

&nbsp;   <button id="show">show button</button> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#hide").click(function(){ 

&nbsp;               $("#text1").hide(); 

&nbsp;           }); 

&nbsp;           $("#show").click(function(){ 

&nbsp;               $("#text1").show(); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html> 

Output: 

&nbsp;                 

**Practical 6 jQuery Advanced:** 



**a) jQuery Animation effects, jQuery Chaining**  

**b) jQuery Callback, jQuery Get and Set Contents**

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>animation</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

&nbsp;   <style> 

&nbsp;       #box{ 

&nbsp;           height: 100px; 

&nbsp;           width: 100px; 

&nbsp;           background-color: green; 

&nbsp;           position: relative; 

&nbsp;       } 

&nbsp;   </style> 

</head> 

<body> 

&nbsp;   <button id="bt">click here for animation</button> 

&nbsp;   <div id="box"></div> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#bt").click(function(){ 

&nbsp;               $("#box").animate({ 

&nbsp;                   left:'250px', 

&nbsp;                   height:'150px', 

&nbsp;                   width:'300px', 

&nbsp;                   opacity:'0.1' 

&nbsp;               },1000); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html> 

Output: 

&nbsp;    

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;                       

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>channing</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <p id="text">watch me chnage</p> 

&nbsp;   <button id="chain">click me</button> 

&nbsp;

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#chain").click(function(){ 

&nbsp;               $("#text").css("color","red").slideUp(1000).slideDown(1000).fadeOut(1000).fadeIn(

&nbsp;1000); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

&nbsp;   </script> 

</body> 

</html> 

Output: 

&nbsp;                                   

&nbsp;

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>jquery callback</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <button id="bt">this will fade the text</button> 

&nbsp;   <p id="text">this will fade out first and then show alert</p> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#bt").click(function(){ 

&nbsp;               $("#text").fadeOut(1000,function(){ 

&nbsp;                   alert("text is hidden now"); 

&nbsp;               }); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html> 

Output: 

&nbsp;

&nbsp;

Code: 

<!DOCTYPE html> 

<html lang="en"> 

<head> 

&nbsp;   <meta charset="UTF-8"> 

&nbsp;   <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

&nbsp;   <title>set and get content</title> 

&nbsp;   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script> 

</head> 

<body> 

&nbsp;   <p id="para">this is the og text</p> 

&nbsp;   <button id="btget">get text</button> 

&nbsp;   <button id="btset">set text</button> 

&nbsp;   <script> 

&nbsp;       $(document).ready(function(){ 

&nbsp;           $("#btget").click(function(){ 

&nbsp;               alert($("#para").text()); 

&nbsp;           }); 

&nbsp;           $("#btset").click(function(){ 

&nbsp;               $("#para").text("this is the new text"); 

&nbsp;           }); 

&nbsp;       }); 

&nbsp;   </script> 

</body> 

</html> 

Output: 

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;



