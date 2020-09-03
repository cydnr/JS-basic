### Javascript 실행과 실습

> 2020.09.03. 언어의 실행방법과 실습환경에 대해 알아본다.



1. **코드의 작성과 실행**

   - 브라우저 : Chrome 기준

   - 에디터 : 메모장(Windows), 텍스트에디트(Mac)

     - ```html
       <!DOCTYPE html>
       <html>
           <head>
               <meta charset="utf-8"/>
           </head>
           <body>
               <script>
                   alert('Hello world');
               </script>
           </body>
       </html>
       ```

       - JS는 html 위에서 동작하기 때문에. html 코드 내의 `<script>` 태그 안에 저장.
       - `파일명.html`으로 저장하고, 브라우저에서 `ctrl+o` 한 뒤에 열면 됨.



2. **콘솔 사용법**

   - 파일에 직접 작성하지 않고 JS를 실행해볼 수 있는 방법
   - Chrome 개발자도구 활용
     - `F12` 혹은 `도구-개발자도구`로 접근
     - 개발자 도구에서 `Show Console`에서 JS 코드만 쳐서 실행해보면 됨. (짧은 것은 이렇게 활용할 때 편리.)
     - 더 알아보고 싶다면 https://opentutorials.org/course/580
     - html 코드에서 script내에 `console.log('Hello World');`라고 작성해서 실행하면, Hello World가 콘솔 창에 떠서 볼 수 있음.

   

3. **도구의 선택**

   - 코드를 작성하는 에디터에는 여러가지 종류가 있음.
     - 마치 백화점처럼 여러가지 기능을 통합해서 제공하는 도구를 통합개발도구(IDE, Integrated Development Environment)라고 함.
     - 에디터 중 하나로 Sublime Text를 소개.
   - 좋은 개발도구를 찾고 사용하는 것이 중요.

