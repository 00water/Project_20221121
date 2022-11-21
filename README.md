JavaScript로 영상을 읽어 화면에 출력하기
================================
수업시간 요약
---------
오늘은 html을 활용하여 각자 컴퓨터에 실습할 폴더를 만들어 메모장으로 인덱스 파일과 자바스크립트 파일을 만들어 인터넷 창으로 자바스크립트를 실행 해보는 시간을 가졌습니다.   
코드는 디지털영상처리 카페를 참조하였습니다.   

코드
---
- html
~~~html
<html>
    <script defer src="rfile.js"></script>
    <input type='file' accept='image/*' onchange='openFile(event)'><br>
    <img id='imageUpload'>
</html>
~~~
- rfile.js
~~~js
var openFile = function(file) {
  var input = file.target;
  var reader = new FileReader();
  reader.onload = function(){
    var dataURL = reader.result;
    var imageUpload = document.getElementById('imageUpload');
    imageUpload.src = dataURL;
  };
  reader.readAsDataURL(input.files[0]);
};
~~~

실행화면
------
![image](https://user-images.githubusercontent.com/105781767/203014578-aba9c14f-bfc0-4d90-b110-11369fcc6dfd.png)
   

크롬 서버를 활용하여 웹에서 자바스크립트 실행하기
=====================================
설명
---
깃허브 주소 https://github.com/WebDevSimplified/Face-Recognition-JavaScript 참조하여 웹에서 실행할 때,   
서버가 응답하지 않아 동작하지 않는 스크립트를 'Web Server for Chrome'을 통해 실행해 보았습니다.

실행화면
------
![image](https://user-images.githubusercontent.com/105781767/203015395-58a515ad-ff53-45c7-a6d2-1eb0602e0767.png)
