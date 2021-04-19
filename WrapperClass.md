 ## 래퍼 클래스(Wrapper Class)

 - 자바의 자료형은 크게 기본 타입(primitive type)과 참조 타입(reference type)으로 나누어집니다.
 - 대표적으로 기본 타입은 char, int, float, double, boolean 등이 있고 참조 타입은 class, interface 등이 있는데 프로그래밍을 하다 보면 기본 타입의 데이터를 
   객체로 표현해야 하는 경우가 종종 있습니다.
 - 이럴 때에 기본 자료타입(primitive type)을 객체로 다루기 위해서 사용하는 클래스들을 래퍼 클래스(wrapper class)라고 합니다. 
 - 자바는 모든 기본타입(primitive type)은 값을 갖는 객체를 생성할 수 있습니다. 이런 객체를 포장 객체라고도 하는데 그 이유는 기본 타입의 값을 내부에 두고 포장하기 때문입니다.
 - 래퍼 클래스로 감싸고 있는 기본 타입 값은 외부에서 변경할 수 없습니다. 만약 값을 변경하고 싶다면 새로운 포장 객체를 만들어야 합니다.

 

### 래퍼 클래스의 종류

| 기본타입(primitive type)|래퍼클래스(wrapper class)|
|----------|:-------------:|------:|
| byte | Byte|
| char | Character|
| int | Integer|
| float | Float|
| double | Double|
| boolean | Boolean|
| long | Long|
| short | Short|

- 래퍼 클래스는 java.lang 패키지에 포함되어 있는데, 다음과 같이 기본 타입에 대응되는 래퍼 클래스들이 있습니다. 
- char타입과 int타입이 각각 Character와 Integer의 래퍼 클래스를 가지고 있고 나머지는 기본 타입의 첫 글자를 대문자로 바꾼 이름을 가지고 있습니다.

<br/>

### 박싱(Boxing)과 언박싱(UnBoxing) 

- 기본 타입의 값을 포장 객체로 만드는 과정을 박싱이라고 하고 반대로 포장객체에서 기본타입의 값을 얻어내는 과정을 언박싱이라고 합니다. 
```
public class Wrapper_Ex {
    public static void main(String[] args)  {
        Integer num = new Integer(17); // 박싱
        int n = num.intValue(); //언박싱
        System.out.println(n);
    }
}
```

<br/>


### 자동 박싱(AutoBoxing)과 자동 언박싱(AutoUnBoxing)

- 기본타입 값을 직접 박싱, 언박싱하지 않아도 자동적으로 박싱과 언박싱이 일어나는 경우가 있습니다. 자동 박싱의 포장 클래스 타입에 기본값이 대입될 경우에 발생합니다.
- 예를 들어 int타입의 값을 Integer클래스 변수에 대입하면 자동 박싱이 일어나 힙 영역에 Integer객체가 생성됩니다.

```
public class Wrapper_Ex {
    public static void main(String[] args)  {
        Integer num = 17; // 자동 박싱
        int n = num; //자동 언박싱
        System.out.println(n);
    }
}
```

