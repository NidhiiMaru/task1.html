# task1.html
<!DOCTYPE html>
<html>
<head>
  <title>Friends Nickname Generator</title>
</head>
<body>

  <h2>Get Your Friends Universe Nickname</h2>

  <label>
    <input type="text" id="firstName" placeholder="Enter your first name">
  </label> 
 <!--id Gives a unique name to access via JS-->

  <button onclick="generateNickname()">Generate</button>
  <!--When this button is clicked, run this JavaScript function.-->
  <br><br>

  <p id="nicknameOutput"></p>

  <script>
    function generateNickname() {
      var firstName = document.getElementById("firstName").value;
      // value gets the actual text from label not just the element.

      if (firstName.length < 1) {
        document.getElementById("nicknameOutput").innerText = "Pleaseee enter your name!";
        return;
        //Find the HTML element that has the id of nicknameOutput
        //Whatever you assign to innerText will replace what's currently there.
      }

      var slicedName = firstName.slice(0, 4);
      var surnames = ["Geller", "Tribbiani", "Buay", "Green", "Bing", "Wheeler", "Hannigan"];
      var randomIndex = Math.floor(Math.random() * surnames.length);
//Math.random()Generates a random decimal number between 0 and just below 1.
//surnames.length is the total number of surnames in your list.If you have 7 surnames, then surnames.length = 7.
//Math.floor(...)This takes any decimal and rounds it down to the nearest whole number.

      var randomSurname = surnames[randomIndex];
                   
      var nickname = slicedName + " " + randomSurname;
      document.getElementById("nicknameOutput").innerText = "Your Friends nickname: " + nickname;
    }
  </script>

</body>
</html>
//comments editted
