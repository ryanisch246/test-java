<html>
    
  <head>
    
   <title>How many fingers?</title>
   
   <style type=text/css>
     
     #numberSelected {
     
     margin-left:15px
     
     }
     
   </style>
   
  </head>
    
  <body>
    
   
      <p>How many fingers are you holding up?</p>
    
      <p><select id="numberSelected">
        
        <option>0</option>
        <option>1</option>
        <option>2</option>
        <option>3</option>
        <option>4</option>
        <option>5</option>
        
        </select>
 
      <button id="guess">Guess</button></p>
      
      <script type="text/javascript">
      
        function doAGuess(correctAnswer) {
          
          var randomNumber = Math.random();
              
              randomNumber = randomNumber * 6;
              
              randomNumber = Math.floor(randomNumber);
              
              if (randomNumber == correctAnswer) {
                
                return(true);
                
              } else {
                
                return(false);
                
              }
          
          
        }
      
        document.getElementById("guess").onclick = function() {
          
          var numberSelected = document.getElementById("numberSelected").value;
          
          var gotIt = false;
          
          var numberOfGuesses = 1;
          
            while (gotIt == false) {
              
              if (doAGuess(numberSelected) == true) {
                
                gotIt = true;
                
                alert ("Got it! It was a " + numberSelected + ", It took me " + + numberOfGuesses + " guesses.");
                
              } else {
                
                numberOfGuesses++;
                
              }
            
            }
        
        }
        
      </script>
      
  </body>
    
</html>
