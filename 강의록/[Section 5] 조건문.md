### Javascript 조건문

> 2020.09.08. JS의 조건문에 대해 알아본다



1. **조건문이란?**
   - conditional statement
   - 주어진 조건에 따라서 애플리케이션을 다르게 동작하도록 하는 것이다.
   - 조건문의 **문법**
     - **if**
       
       - 조건문은 if로 시작한다. if 뒤의 괄호에 조건이 오고, 조건이 될 수 있는 값은 `Boolean`이다. Boolean의 값이 `true`라면 조건이 담겨진 괄호 다음의 중괄호 구문이 실행된다.
       
       - ```js
         if(true){
             alert('result : true');
         } // alert로 result : true 출력
         
         if(false){
             alert('result : true');
         } // 출력 없음
         ```
       
       - ```js
         if(true){
             alert(1);
             alert(2);
             alert(3);
             alert(4);
         }
         alert(5); // 1,2,3,4,5 차례로 출력
         
         if(false){
             alert(1);
             alert(2);
             alert(3);
             alert(4);
         }
         alert(5); // 5만 출력
         ```
       
     - **else**
     
       - `if`만으로는 좀 더 복잡한 상황을 처리하기엔 부족하다.
     
       - 거짓일 때 어떻게 처리할 지 결정하는 역할
     
       - ```js
         if(true){
             alert(1);
         } else {
             alert(2);
         } // 출력은 1
         
         if(false){
             alert(1);
         } else {
             alert(2);
         } // 출력은 2
         ```
     
     - **else if**
     
       - `else if`를 사용하면 조건문을 좀 더 풍부하게 할 수 있다.
     
       - ```js
         if(false){
             alert(1);
         } else if(true){
             alert(2);
         } else if(true){
             alert(3);
         } else {
             alert(4);
         } // 결과 : 2
         
         if(false){
             alert(1);
         } else if(false){
             alert(2);
         } else if(true){
             alert(3);
         } else {
             alert(4);
         } // 결과 : 3
         
         if(false){
             alert(1);
         } else if(false){
             alert(2);
         } else if(false){
             alert(3);
         } else {
             alert(4);
         } // 결과 : 4
         ```
     
       
   
2. **조건문의 응용**

   - **변수와 비교연산자**

     - 앞서 배운 변수와 비교연산자, 그리고 조건문을 결합해보자.

     - ```html
       <!DOCTYPE html>
       <html>
       <head>
           <meta charset="utf-8"/>
       </head>
       <body>
           <script>
               id = prompt('아이디를 입력해주세요.')
               if(id=='myid'){
                   alert('아이디가 일치 합니다.')
               } else {
                   alert('아이디가 일치하지 않습니다.')
               }
           </script>
       </body>
       </html>
       ```

       - `prompt` : 입력을 받아오는 프롬프트 창을 띄울 수 있음

         ```js
         alert(prompt('Your age?')) // 여기서 20치면, 40 출력
         ```

       - 위의 코드는 입력으로  `myid`가 들어오면 `아이디가 일치 합니다.` 출력, 다른 것을 입력하면 `아이디가 일치하지 않습니다.` 출력.

       - 이런 식으로 `로그인` 로직 구현.

     - ```html
       <!DOCTYPE html>
       <html>
       <head>
           <meta charset="utf-8"/>
       </head>
       <body>
           <script>
               id = prompt('아이디를 입력해주세요.');
               if(id=='egoing'){
                   var password = prompt('비밀번호를 입력해주세요.');
                   if(password==='111111'){
                       alert('로그인 되었습니다.');
                   } else {
                       alert('비밀번호가 일치하지 않습니다. '+id+'님 반갑습니다.');
                   }
               } else {
                   alert('아이디가 일치하지 않습니다.');
               }
           </script>
       </body>
       </html>
       ```

       - 조건문 내에 조건문을 넣을 수 있음.

       

3. **논리 연산자**

   - 논리연산자는 조건문을 좀 더 간결하고 다양한 방법으로 구사할 수 있도록 도와준다.

   - **&&** (AND)

     - `&&`는 좌항과 우항이 모두 참일 때 참이 된다.

     - ```js
       if (true && true) {
           alert(1);
       }
       if (true && false) {
           alert(2);
       }
       if (false && false){
           alert(3);
       } // 결과 : 1
       ```

     - 활용

       ```html
       <!DOCTYPE html>
       <html>
       <head>
           <meta charset="utf-8"/>
       </head>
       <body>
           <script>
               id = prompt('아이디를 입력해주세요.');
               password = prompt('비밀번호를 입력해주세요.');
               if(id=='myid' && password=='111111'){
                   alert('로그인 했습니다. '+id+'님 반갑습니다.);
               } else {
                   alert('인증에 실패 했습니다.');
               }
           </script>
       </body>
       </html>
       ```

   - **||** (OR)

     - `||`는 좌우항 중에 하나라도 참이라면 참이 되는 논리 연산자이다.

     - ```js
       if (true || true) {
           alert(1);
       }
       if (true || false) {
           alert(2);
       }
       if (false || false){
           alert(3);
       } // 결과 : 1, 2
       ```

     - 활용

       ```js
       id = prompt('아이디를 입력해주세요.');
       password = prompt('비밀번호를 입력해주세요.');
       if((id==='myid' || id==='urid' || id==='thisid') && password==='111111'){
           alert('인증 했습니다.');
       } else {
           alert('인증에 실패 했습니다.');
       }
       ```

       - `id`값이 `myid`, `urid`, `thisid` 중에 하나이고, `password`가 `111111`이라면 인증해주는 코드

   - **!** (NOT)

     - `!`는 부정의 의미로, Boolean 값을 역전시킨다. `true`를 `false`로, `false`를 `true`로 만든다.

     - ```js
       if (!true && !true) {
           alert(1);
       }
       if (!true && !false) {
           alert(2);
       }
       if (!false && !false){
           alert(3);
       } // 결과 : 3
       ```

     

4. **Boolean의 대체재**

   - 조건문에 사용될 수 있는 데이터 형이 꼭 Boolean만 되는 것은 아니다. 관습적인 이유로, `0`은 `false`, 0이 아닌 값은 `true`로 간주된다.

     ```js
     if(0){
         alert(1);
     }
     if(1){
         alert(2);
     }  // 결과 : 2
     ```

   - 기타 false로 간주되는 데이터형

     ```js
     if(!''){
         alert('빈 문자열');
     }
     if(!undefined){
         alert('undefined');
     }
     var a;
     if(!a){
         alert('값이 할당되지 않은 변수')
     }
     if(!null){
         alert('null');
     }
     if(!NaN){
         alert('NaN');
     }
     ```

     

