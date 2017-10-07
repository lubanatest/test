 <html>
 
   <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script> 
   <script type="text/javascript" src="graph.js"></script>
<script type="text/javascript" src="findPath.js"></script>

<script>
  
  function validateForm() {
  
      submitForm() ;
  }
  
  // ---------------------
  
  
  function submitForm() {
     var csv = document.forms["myForm"]["csv"].value;
     // read CSV file content and save it to Graph
-    
+    var graph = readCSV(); 
 //graph.print();
   
   // Get entered data
   var x = document.forms["myForm"]["from"].value;
   var y = document.forms["myForm"]["to"].value;
   var t = document.forms["myForm"]["time"].value;
   
-  
+  //findPath(graph,x,y,t);
   
      
   } 
</script>

 <body ng-app=""> 
 
 # Test
Developer Test


 <h3>Enter the following information please:</h3>
 
 <form name="myForm">
  <table >
  <tr>
   
   <td >CSV File:</td>
   <td ><input type="file" name="csv" id="csv" onchange="" ng-model="csv" required/>
   <div id="csvError" ng-show="myForm.csv.$invalid">required</div>
   </td>
   
  </tr>
  <tr>
   <td >Device from: </td>
   <td ><input type="text" name="from" ng-model="from" required>
    <div id="fromError" ng-show="myForm.from.$invalid">required</div></td>
  </tr>
   <tr><td >Device to: </td><td ><input type="text" name="to"></td></tr>
   <tr><td >Time: </td><td ><input type="text" name="time"></td></tr>
  
  <tr><td  colspan="2"><input type="button" onclick="validateForm()" value="ok" /></td></tr>
  
  </table>
  
 </form>
 </body>
</html>
