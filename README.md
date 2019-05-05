
<html>
<head>
<script>
function insert(num)
{
document.form.textview.value=document.form.textview.value+num;
}
function equal()
{
var x=document.form.textview.value
if(x){
document.form.textview.value=eval(x)
}}
function clean(){
document.form.textview.value="";
}
function back(){
var x=document.form.textview.value;
document.form.textview.value=x.substring(0,x.length-1);
}
</script>
<style>
.button{
width:50;
height:40;
font-size:25;
cursor:pointer;
}
#textview{
width:230;
height:40;
border:10px;
padding:10;
font-size:25;
}
.main{
position:absolute;
top:30%;
left:40%;
}
#watermark{
font-size:100;
color:#d0d0d0;
width:100;
height:100;
position:absolute;
z-index:-1;
left:27%;
webkit-transform:rotate(-45deg);
-moz-transform:rotate(-45deg);
}
</style>
</head>
<body bgcolor=orange>
<div id=watermark>CALCULATOR</div>
<div class="main">
<form name="form">
<input type="text" id="textview" name="textview">
</form>
<table bgcolor=#00FF00 border=2>
<tr>
<td><input class="button" type="button" value="C" onclick="clean()"></td>
<td><input class="button" type="button" value="<" onclick="back()"></td>
<td><input class="button" type="button" value="/" onclick="insert('/')" ></td>
<td><input class="button" type="button" value="x" onclick="insert('*')" ></td>
</tr>
<tr>
<td><input class="button" type="button" value="7" onclick="insert(7)" ></td>
<td><input class="button" type="button" value="8" onclick="insert(8)" ></td>
<td><input class="button" type="button" value="9" onclick="insert(9)" ></td>
<td><input class="button" type="button" value="-" onclick="insert('-')" ></td>
</tr>
<tr>
<td><input class="button" type="button" value="4" onclick="insert(4)" ></td>
<td><input class="button" type="button" value="5" onclick="insert(5)" ></td>
<td><input class="button" type="button" value="6" onclick="insert(6)" ></td>
<td><input class="button" type="button" value="+" onclick="insert('+')" ></td>
</tr>
<tr>
<td><input class="button" type="button" value="1" onclick="insert(1)" ></td>
<td><input class="button" type="button" value="2" onclick="insert(2)" ></td>
<td><input class="button" type="button" value="3" onclick="insert(3)" ></td>
<td rowspan=2><input class="button" style="height:80" type="button" value="=" onclick="equal()" ></td>
</tr>
<tr>
<td colspan=2><input class="button" style="width:100"type="button" value="0" onclick="insert(0)" ></td>
<td><input class="button" type="button" value="." onclick="insert('.')"></td>
</tr>
</table>
</div>
</body>
</html>
