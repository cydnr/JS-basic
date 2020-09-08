### Javascript 비교

> 2020.09.08. JS의 비교 연산(대입, 동등, 일치, 부정, 부등호)에 대해 알아본다



1. **연산자란?**

   - 연산자란 값에 대해서 어떤 작업을 컴퓨터에게 지시하기 위한 기호

   - ex. `a = 1`

     - `=`는 '대입연산자'이다. (이항연산자 중 하나.)
     - `a`는 변수, `1`은  값(또는 상수).

     

2. **비교 연산자**

   - 프로그래밍에서 비교란 주어진 값들이 같은지, 다른지, 큰지 작은지를 구분하는 것을 의미한다. 이때 비교 연산자를 사용하는데, 비교연산자의 결과는 `true`나 `false` (-> `boolean` 타입) 중 하나이다.

   - **동등 연산자**

     - `==` , equal operator

     - 좌항과 우항을 비교해서 서로 같다면 `true`, 다르다면 `false`가 된다.

     - ```js
       alert(1==2)             // false
       alert(1==1)             // true
       alert("one"=="two")     // false 
       alert("one"=="one")     // true
       ```

       - `1`과 `'1'`을 같은 것으로 보는 것은 편리해보일 수 있어도, 코드가 커질 수록 이 때 발생한 문제를 해결하기 어려움.

   - **일치 연산자**

     - `===`, strict equal operator

     - 좌항과 우항이 정확하게 같을 때 `true`, 다르면 `false`가 된다.

     - ```js
       alert(1=='1');              //true
       alert(1==='1');             //false
       ```

       - 값 뿐만 아니라 자료형까지 같아야 `===`이 equal.

   - 동등연산자와 일치연산자

     - 참고 : https://dorey.github.io/JavaScript-Equality-Table/

     - `null` & `undefined`  

       - `null`은 값이 없음을, `undefined`는 값이 정의되지 않았음을 의미.
         - `null`의 자료형은 `null`, `undefined`의 자료형은 `undefined`

       - ```js
         var a;
         alert(a); // undefined
         a = null
         alert(a); // null
         ```

       - 똑같이 값이 없는 상태인데 `null`은 의도적으로 값이 없이 비워둔 것, `undefined`는 의도하지 않게 빈 곳.

       - ```js
         alert(null == undefined);       //true
         alert(null === undefined);      //false
         ```

     - `true` & `1`

       - js에서 `1`은 true, `1`이 아닌 수는 false로 간주.

       - ```js
         alert(true == 1);               //true
         alert(true === 1);              //false
         alert(true == '1');             //true
         alert(true === '1');            //false
         ```

     - `0`과 `-0`

       - ```js
         alert(0 === -0);                //true
         ```

     - `NaN`

       - `0/0`과 같은 연산의 결과로 만들어지는 특수한 데이터형, 숫자가 아니라는 뜻.

       - ```js
         alert(NaN === NaN);             //false
         ```

       

3. **부정과 부등호**

   - 부정

     - `!`는 부정을 의미한다.

     - '같다'의 부정은 '같지 않다'이다. 기호로는 `!=`로 표시한다.

     - `!==`는 정확하게 같지 않다는 의미다.

     - ```js
       alert(1!=2);            //true
       alert(1!=1);            //false
       alert("one"!="two");    //true
       alert("one"!="one");    //false
       ```

   - 부등호

     - ```js
       alert(10>20);   //false
       alert(10>1);    //true
       alert(10>10);   //false
       
       alert(10>=20);      //false
       alert(10>=1);       //true
       alert(10>=10);      //true
       ```

       

