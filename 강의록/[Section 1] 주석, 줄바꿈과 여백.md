### Javascript 주석, 줄바꿈과 여백

> 2020.09.03. JS의 주석, 줄바꿈 및 여백에 대해 알아본다.



1. **주석?**

   - 주석 처리

     - `// comment` 한 줄 주석 처리는 이와 같이.

     - `//` 뒤에 등장하는 내용은 주석이니, 문법적으로 해석하지 말라는 의미.
     - `/* 여러줄 주석 처리는 이렇게 */`

   - 잘 만들어진 코드는 좋은 주석을 가지고 있는 코드. 적합한 형태의 설명을 가진 코드.

   - 미래에 타인이 되어있을 자기 자신, 혹은 협업하는 타인을 위해 주석 사용.



2. **줄바꿈과 여백**

   - ```js
     var a = 1;
     alert(a);
     ```

     - `;`는 명령이 끝났음을 명시적으로 표시.
       - 하지만 줄바꿈이 있으면 명령이 끝났음을 알기 때문에 없어도 동작은 함.
       - `var a = 1; alert(a);`와 같이 한 줄에 넣고 싶다면 필수적.

   - `tab`은 4-spaced로 가독성을 높이기 위해 사용.

