```kotlin
package Interfaces  
  
//코틀린에선 기본적으로 클래스를 상속할 수 없음  
//최상위 부모는 Any임 (java에선 Object)  
//추상 클래스  
//abstract로 클래스, 변수, 함수 모두 선언함  
//클래스 내부에 구현된 함수가 존재할 수 있음  
//추상 클래스를 인스턴스로 직접 생성할수는 없음  
//추상 클래스는 1개만 상속받을 수 있음  
//abstract class Product(val name: String, var price: Double) {  
//    // 상품 카테고리를 담을 추상 프로퍼티  
//    abstract val category: String  
//  
//    // 모든 상품이 공유하는 함수  
//    fun productInfo(): String {  
//        return "Product: $name, Category: $category, Price: $price"  
//    }  
//}  
  
//위 product 클래스를 상속받는 객체  
//class Electronic(name: String, price: Double, val warranty: Int) : Product(name, price) {  
//    override val category = "Electronic"  
//}  
  
//추상화된 객체, 변수는 override를 통해 구현 해줘야한다.  
  
//인터페이스  
//인스턴스를 만들 수 없음  
//인터페이스는 기본적으로 Open 상태  
//open 상태는 상속 받을 수 있는 상태를 말함 kotlin에서는 기본이 close//이외는 java와 똑같으니 설명 생략  
  
//위임  
//인터페이스에서 특정 값만 바꾸고 싶을 때  
//kotlin에서는 by를 이용해 구현을 다른 인스턴스에 위임할 수 있음  
//class CanvasSession(val tool: DrawingTool) : DrawingTool by tool {  
//    override val color = "blue"  
//}  
//위 코드같은 경우엔 DrawingTool의 구현을 tool에게 위임한 것  
//인자로 DrawingTool 인터페이스를 구현한 객체를 넣어주면 나머지 함수들은 tool에 있던 것들을 가져옴
```
