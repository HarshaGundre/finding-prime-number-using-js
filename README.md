<!doctype html>
<html>
<head>
<title>Prime Number Generator</title>
<style>
 body{
 background-color:lightblue;
}
 table{
 background-color:#f2b305;
 
 }
</style>
<script>	
 function is_Prime(num){
  if(num==1)
  {
   return false;
  }
  for(a=2;a<num;a++)
  {
   if(num%a==0)
   {
    return false;
   }
  }
  return true;
  }
 function genrate_prime()
 {
  var start,end,prime="";
  start=parseInt(document.getElementById("t1").value);
  end=parseInt(document.getElementById("t2").value);
  for(b=start;b<=end;b++)
  {
     if(is_Prime(b)==true)
     {
       prime=prime+b.toString()+",";
      //document.write(a);
     }
  }
   document.getElementById("ans").innerHTML=prime.substring(0,prime.length-1);;
 }
 </script>
 </head>
 <body>
  <h1 align="center">Prime Number Generator</h1>
  <form name="frm1">
  <table border="0" cellpadding="5px" cellspacing="0" width="60%" align="center">
  <tr>
    <td>Start</td>
    <td><input type="number" min="1" max="1000" id="t1"/> </td>							
  </tr>	
  <tr>
    <td>End</td>
    <td><input type="number" min="1" max="10000" id="t2"/>  </td>							
  </tr>
  <tr>
    <td>Prime Number</td>
    <td><textarea rows="4" cols="30" id="ans"></textarea></td>							
  </tr>
  <tr>
    <td></td>
    <td><input type="button" value="Generate" onclick="genrate_prime()"/></td>							
  </tr>
 </table>
 </form>
</body>
</html>
