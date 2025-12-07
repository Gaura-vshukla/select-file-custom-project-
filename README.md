<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   <style> 
   *{
    margin:0;
    padding:0;
    box-sizing: border-box;
font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;


}
html,body{
    height:100%;
    width:100%;

}
input{
    display: none;
}
#main{
    display: flex;
    align-items:center;
    justify-content: center;
    height:100%;
    width: 100%;
   background-color: #222 ;
    
}
#btn{
    padding: 12px 22px ;
    background-color: red;
    color: white;
    border-radius: 5px;
    font-weight: 600px;
}
#btn:hover{
    background-color: rgb(13, 218, 150);
}
</style>
</head>
<body><div id="main">
<input type="file" id="fileinp">
<div id="btn">
Uploding file
</div>
</div>
    <script src="card.js"></script>
    
</body>
</html>


//js code for selecting file

let fileinp=document.querySelector("#fileinp");
let btn=document.querySelector("#btn");
btn.addEventListener("click",()=>{
fileinp.click();
});
fileinp.addEventListener("change",(dets)=>{
const file=dets.target.files[0];
if(file){
    btn.textContent=file.name;
}
});
