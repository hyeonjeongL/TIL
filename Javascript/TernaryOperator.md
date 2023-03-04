<h3>삼항 연산자(ternary operator)</h3>
<br>
<h5>삼항 연산자(ternary operator)는 조건 연산자(conditional operator)라고도 불림. 조건문을 간결하게 표현할 수 있는 연산자<h5>
<br>

`(condition) ? (value if true) : (value if false)`

condition은 평가 결과가 참 또는 거짓인 식이며, value if true는 조건식이 참일 때 반환되는 값이고, value if false는 조건식이 거짓일 때 반환되는 값<Br>

`let totalCnt = totalCnt > 2000 ? 2000 : totalCnt;`
<br>
<br>
if else 문을 간단하게 삼항연산자로 표현 가능
<br>
단, 주의할 점은 삼항 연산자는 코드의 가독성을 향상시킬 수 있지만 너무 복잡한 조건식을 사용하면 오히려 가독성이 떨어질 수 있으므로 적절히 사용해야 한다.



