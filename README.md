          <!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Number Guessing Game</title>
  
    <style>
  body {
        padding: 25px;
        background-color: white;
        color: black;
        font-size: 25px;
      }
      .dark-mode {
        background-color: black;
        color: white;
      }
      .light-mode {
        background-color: white;
        color: black;
    </style>
</head>
  
<body>
<h1>Guess The Number</h1>
  
<p>I have selected a number between 1 and 20; can you guess it?. 
See if you can guess it.</p>
  
<div class="form">
    <label for="guessField">Enter a guess: </label>
    <input type = "text" id = "guessField" class = "guessField">
    <input type = "submit" value = "Submit guess" 
           class = "guessSubmit" id = "submitguess">
</div>
  
<script type = "text/javascript">
  
    // random value generated
    var y = Math.floor(Math.random() * 20 + 1);
      
    // counting the number of guesses
    // made for correct Guess
    var guess = 1;
      
    document.getElementById("submitguess").onclick = function(){
      
   // number guessed by user     
   var x = document.getElementById("guessField").value;
  
   if(x == y)
   {    
       alert("YAY! You guessed correctly! Bruh."
               + guess + " GUESS ");
   }
   else if(x > y) /* if guessed number is greater
                   than actual number*/ 
   {    
       guess++;
       alert("Try a smaller number.");
   }
   else
   {
       guess++;
       alert("Try a greater number.")
   }
}
</script>
</body>
</html>                
