```kotlin
package org.example.Collection  
  
fun main(){  
    //List  
  
    //readOnlyList 불변 리스트는 List로 선언  
    val readOnlyList = listOf("김치찌개", "참치탕", "타코");  
    println(readOnlyList);  
  
    //가변 리스트 선언 꺾쇠 가로로 타입 명시 가능  
    val shapes : MutableList<String> = mutableListOf("김치찌개", "참치탕", "타코");  
    println(shapes);  
  
    //불변 리스트 변수에 가변 리스트를 담을 수도 있음  
    //이를 casting 이라고 함  
    val readOnlyList02: List<String> = shapes;  
  
    //요소는 index로도 가져올 수 있고  
    //함수를 통해서도 가져올 수 있음  
    println("나는 오늘 ${readOnlyList02[2]}가 먹고싶어요");  
    println("나는 오늘 ${readOnlyList02.first()}가 먹고싶어요");  
  
    //in 연산자를 통해서 리스트 안에 요소가 존재하는지 확인할 수 있음  
    //boolean 값을 리턴함  
    println("타코" in readOnlyList02);  
  
    //요소 추가 삭제는 각각 .add(), .remove() 메서드를 통해 진행  
    shapes.add("감자튀김");  
    shapes.remove("김치찌개");  
    println(shapes);  
  
}
```

<hr>

같이 보면 좋은 내용들
- [[List]]
- [[Set]]
- [[Collection]]