---
title: "유니코드 변환기를 만들어 보았습니다."
date: 2020-09-28 09:06:28 -0400
categories: unicord
---
유니코드 변환기를 이번에 한 번 만들어 보았습니다.
이거 유니코드 변환기가 생각보다 만들기 쉽네요^^

링크 공유 - https://zzstudio-dev.github.io/devtool/unicord.html

소스코드도 공유합니다^^


<pre>
<code>
<!DOCTYPE html>
<html lang="한글">
<head>
    <meta charset="UTF-8">
    <title>유니코드 번역기</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous">
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
    <script>

	function replaceAll(strTemp, strValue1, strValue2){ 

            while(1){

                if( strTemp.indexOf(strValue1) != -1 )

                    strTemp = strTemp.replace(strValue1, strValue2);

                else

                    break;

            }

            return strTemp;

     }

	 function unicodeToKor(){

	 //유니코드 to 한글

		var str=document.getElementById("a").value;

		document.getElementById("b").value=unescape(replaceAll(str, "\\", "%"));

	 }

	 

	 function korToUnicode(){

	 //한글 to 유니코드

		var str=document.getElementById("aa").value;

		document.getElementById("bb").value=escape(replaceAll(str, "\\", "%"));

		

	 }

</script>
</head>
<body>
 
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="">ZZ Studio Developement tools</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="">Unicode transform <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="" tabindex="-1" aria-disabled="true">Comming soon</a>
      </li>
    </ul>
  </div>
</nav>
  <br>
  <br>
  <br>
   <center>    <input type="text" id="a"/ ><a href="javascript:unicodeToKor()"><button type="button" class="btn btn-primary">유니코드 to ᄒᆞᆫ글</button></a> <input type="text" id="b"/>

<br><br><br>

<input type="text" id="aa"/><a href="javascript:korToUnicode()"><button type="button" class="btn btn-primary">ᄒᆞᆫ글 to 유니코드</button></a> <input type="text" id="bb"/></center>

</body>
</html>
</code>
</pre>
