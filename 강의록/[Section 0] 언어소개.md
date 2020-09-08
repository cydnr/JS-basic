### Javascript 언어소개

> 2020.09.03.



1. **JS ?**

   - JS와 **웹브라우저**

     - JS를 이야기 할 때 웹브라우저를 빼놓을 수 없다.

     - JS는 웹브라우저로 분류되는 SW를 프로그래밍적으로 제어하기 위한 언어.

       - 프로그래밍적 제어?

         - ```html
           <html>
               <body>
                   <input type="button" onclick="alert('Hello world')" value="Hello world">
               </body>
           </html>
           ```

         - 위와 같은 코드를 작성하면, 브라우저에 Hello world라는 버튼을 만들어주고, 클릭 시 경고창에 Hello world 출력.

         - `alert('Hello world')`가 JS. 이를 통해 경고창을 띄우는 프로그래밍적 제어를 할 수 있는 것.

   - JS와 **탈웹브라우저**

     - 최근 JS라는 언어에서 대두되는 흐름.

     - 더 이상 웹브라우저를 제어하기 위한 용도로만 사용되지 않는 JS.

     - JS라는 언어와 동작하는 환경(ex. 웹브라우저)를 분리해서 생각해야할 필요성 대두

       - Q. 그렇다면 어떤 곳에 사용할 수 있을까? A. 웹서버

     - 웹서버를 동작하기 위한 도구로 기능할 수 있음. Server-side-script.

       - 그 중 대표적으로 Node.js

       - ![image-20200903212412923]([Section 0] 언어소개.assets/image-20200903212412923.png)

         - 이렇게 사용하면 웹서버, 브라우저 모두 js로 통일시킬 수 있다는 장점

       - ```js
         var http = require('http')
         http.createServer(function(req,res){
             res.writeHead(200, {'Content-Type':'text/plain'});
             res.write('Hello World\n');
             res.end();
         })listen(1337, '127.0.0.1');
         console.log('Server running at http://127.0.0.1:1337/');
         ```

         - 웹서버에서 js가 활용되는 구체적 사례.
         - js의 문법에 따라 Nodejs를 제어하는 코드. 이를 통해 Hello World를 출력.
         - `node 파일명.js`으로 실행. 1337이라는 포트에서 Hello World 출력.

   - JS와 **탈웹**

     - JS가 Web 바깥에서도 쓰이기 시작.

     - 대표적 예로 `Google Apps Script`

       - `구글 스프레드 시트 - 스크립트 편집기 - 빈 프로젝트`로 추가.

         ```js
         function onOpen() {
             var name = Browser msgBox('Hello world');
         }
         ```

         - 구글 스프레드시트가 가지고 있는 기능인 Message box에 Hello World를 담아서 출력

           

2. **언어**란?

   - 의사소통을 위한 **약속**

   - 프로그래밍 언어의 문법(=약속)을 통해 컴퓨터에게 일을 시킬 수 있는 것

     

3. **환경**이란?

   - 언어와 언어가 동작하는 환경을 분리해서 생각하면 효용이 있음.
   - 언어를 사용하는 대상이 환경.
   - ![image-20200903213646720]([Section 0] 언어소개.assets/image-20200903213646720.png)
     - `~해주세요`하는 것은 언어. 그러나 대화하는 상대의 역할에 따라 해주세요, 하더라도 일을 할 수 없는 경우가 있음. 어떤 환경에서 언어를 사용하는지가 중요하다는 의미.
   - ![image-20200903213924182]([Section 0] 언어소개.assets/image-20200903213924182.png)
     - JS를 활용해서 각 환경에 맞도록 명령을 사용해야한다는 것.
     - 언어라는 공통분모를 가지고 환경을 제어하는데, 각 환경에 따라 할 수 있는 일이 따르고, 명령하기 위한 명령어가 다르다는 뜻.