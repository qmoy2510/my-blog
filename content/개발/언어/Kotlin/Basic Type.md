
## 코틀린에서의 변수 선언

코틀린에서는 변수를 선언 할 떄 
**var**(variable)와 **val**(value)을 이용한다.

---
## var
- 변수를 선언할 때 사용
- 타입 추론 기능이 내장 되어있음
- 선언'만' 하는건 불가능함

아래 코드는 var를 이용한 예시 코드임
```kotlin
package org.example  
fun main() {  
    //타입 추론으로 Int 타입을 가지게 됨
    var custmoer = 10;   
    
    //값이 없으므로 타입을 추론할 수 없음
    //-> 에러 발생
    var custmoer;   
  
    custmoer = 8;  
    custmoer += 3;  
    custmoer -= 6;  
    custmoer *= 5;  
    custmoer /= 1;  
    println(custmoer);  
    //25 출력 
}
```

### 타입 명시
var 변수 선언할 때엔 타입을 명시해서 적어줄 수도 있음

타입을 명시하게 되면 값을 비워두고 선언만 할 수도 있음

타입 명시는 아래와 같이 하면 됨
**var (변수명): (변수타입) = (값)**

```kotlin
package org.example  
fun main() {  

    var year: Int;  
    var name: String = "남병철";  
  
    println(name);  
    //남병철 출력
}
```
