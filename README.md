# City of Lubbock

## Solid Waste Management

Welcome to The City of Lubbock Solid Waste Management site. At this new website you may submit reports and/or requests about how your trash is managed. You may also use this site to view if your trash has been picked for this week.

To submit a service request, follow the instructions below:

<html>
<body>

<h2>Enter Your First and Last Name</h2>

<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
</form>

<h2>Enter Your Six Digit Code</h2>
<form>
  <label for="six digit code">Six Digit Code:</label><br>
  <input type="password" id="six digit code" name="six digit code" value="123456"><br><br>
</form>

<h2>Enter Your Service Request</h2>
<form>
  <label for="lname">Type your issue with your trash bin below:</label><br>
  <input type="text" id="lname" name="lname" value="QR Code ripped off."><br><br>
  <input type="submit" value="Submit">
</form> 

<h2>(Optional): Upload Images of Trash Bin</h2>
<form>
<input type="file" accept="image/*" id="file" name="image" onchange="loadFile(event)" style="display: none;">
</form> 
<p><label for="file" style="curser: pointer;">Upload Image</label></p>
<p><img id="output" width="200" /></p>

<p><label for="file" style="curser: pointer;">Upload Image</label></p>
<p><img id="output" width="200" /></p>

<script>
var loadFile = function(event)	{
	
	var image = document.getElementById('output');

	image.src = URL.createObjectURL(event.target.files[0]);

};

</script>

</body>
</html>

<html>
<body>
<script src="best.js">
</script>
</body>
</html>

<html>
   <head>

      <script type = "text/javascript">
         var db = openDatabase('mydb', '1.0', 'Test DB', 2 * 1024 * 1024);
         var msg;

         db.transaction(function (tx) {
            tx.executeSql('CREATE TABLE IF NOT EXISTS LOGS (id unique, log)');
            tx.executeSql('INSERT INTO LOGS (id, log) VALUES (1, "foobar")');
            tx.executeSql('INSERT INTO LOGS (id, log) VALUES (2, "logmsg")');
            msg = '<p>Log message created and row inserted.</p>';
            document.querySelector('#status').innerHTML =  msg;
         })

         db.transaction(function (tx) {
            tx.executeSql('SELECT * FROM LOGS', [], function (tx, results) {
               var len = results.rows.length, i;
               msg = "<p>Found rows: " + len + "</p>";
               document.querySelector('#status').innerHTML +=  msg;

               for (i = 0; i < len; i++) {
                  msg = "<p><b>" + results.rows.item(i).log + "</b></p>";
                  document.querySelector('#status').innerHTML +=  msg;
               }
            }, null);
         });
      </script>
   </head>

   <body>
      <div id = "status" name = "status">Status Message</div>
   </body>
</html>

<html>
<head>
<title>Test Input </title>
<script LANGUAGE="JavaScript">
function readText (form) {
    TestVar =form.inputbox.value;
    alert ("You typed: " + TestVar);
}
function writeText (form) {
    form.inputbox.value = "Have a nice day!"
}
</script>
</head>
<body>
<form NAME="myform" ACTION="" METHOD="GET">
Enter something in the box: <br>
<input TYPE="text" NAME="inputbox" VALUE=""><p>
<input TYPE="button" NAME="button1" Value="Read" onClick="readText(this.form)">
<input TYPE="button" NAME="button2" Value="Write" onClick="writeText(this.form)">
</form>
</body>
</html>

<html>
<p><input type="file" accept="image/*" name="image" id="file" onchange="loadFile(event)" style="display: none;"></p>
<p><label for="file" style="cursor: pointer;">Upload Image</label></p>
<p><img id="output" width="200" /></p>

<script>
var loadFile = function(event)	{
	
	var image = document.getElementById('output');

	image.src = URL.createObjectURL(event.target.files[0]);	

};
</script>
</html>

<!--
#URL:https://www.javaworld.com/article/2077176/using-javascript-and-forms.html
#URL:https://stackoverflow.com/questions/21396279/display-image-and-validation-of-image-extension-before-uploading-file-using-java
#URL:https://stackoverflow.com/questions/8810927/showing-an-image-from-an-array-of-images-javascript
#URL:https://stackoverflow.com/questions/21396279/display-image-and-validation-of-image-extension-before-uploading-file-using-java
#URL:https://codewithlogic.wordpress.com/2013/09/01/creating-a-file-uploader-using-javascript-and-html-5/
#URL:https://www.webtrickshome.com/faq/how-to-display-uploaded-image-in-html-using-javascript
-->
