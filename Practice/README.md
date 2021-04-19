## 문자열 다루기 / String

```
String str=””;

 

str.charAt(int index);

str.indexOf(String find);  

str.indexOf(String find, int from);

str.contains(String str);

 

str.toCharArray();

str.split(“”)   // 각 문자들을 리스트로 만들거면 String[]을 사용하는 것이 편함

 

integer to String : Integer.toString(int i);   // str = “” + i;

char to String : Character.toString(char c);  // str = “”+ c;

String to int : Integer.parseInt(str);

 

String sub = str.substring(int start, int end); // end 포함 안됨

 

str.toUpperCase();  str.toLowerCase();

str.length();
```
 

## 문자열 다루기 / StringBuilder
```
StringBuilder sb = new StringBuilder();

StringBuilder sb = new StringBuilder(String str);

StringBuilder sb = new StringBuilder(char[] chars);

 

sb.append();

sb.insert(int index, String str);  // 위치에 삽입할때는 insert

 

sb.charAt(int index);

sb.indexOf(String str);

 

sb.substring(int start, int end);

 

sb.replace(int start, int end, String str);

 

sb.delete(int start, int end);

 

sb.reverse()

 

sb.length();

sb.toString();
```
 

 

## 기본형 다루기 / Integer, Character

```
char to int : Character.getNumericValue(char c);  // int i = c – ‘a’;

char to String : Character.toString(char c); // String str = “”+c;

             : String str = String.valueOf(char c);    // nullPointerException 없음

             : String str = new String(char[] cArray);

int to String : Integer.valueOf(int i)

 

Character.isDigit();

 

String binaryStr = Integer.toBinaryString(int num);

String hexString= Integer.toHexString(int num);

String octalString= Integer.toOctalString(int num);

 

int i = Integer.parseInt(binaryStr, 2);

 

Math.ceil();  

Math.floor(); 

Math.sqrt();  

Math.pow(int i, int p);

Math.max(int a, int b);

Math.min(int a, int b);

Math.round(double d);

Math.abs(int i);
```
 

 

## 배열 다루기
```
Arrays.sort(T[] arrays)

Arrays.sort(T[] arrays, Collections.reverseOrder());

Arrays.sort(T[] arrays, new Comparator<T>(){

    public int compare(T o1, T o2){ return i;}

})

 

Arrays.asList(T[] arrays);   // java.util.Arrays.ArrayList 크기 변경 불가

List converted = new List(Arrays.asList(arrays));

 

Arrays.copyOf(T[] arr, int length);

Arrays.fill(T[] arr, Object o);

 

Arrays.binarySearch(T[] arr, Object key)  // 정렬 후 사용, 값 중복 시 인덱시 랜덤
```
 

 

## 리스트 다루기

```
T[] arrays = list.toArray(new T[size]);  //minimum size는 list.size()

 

Collections.sort(collections c);

Collections.sort(collections c, Collections.reverseOrder());

Collections.sort(collections c, new comparator<T>(){

   public int compare(T ob1, T ob2){return i;}       

})
```
 

List -> ArrayList, LinkedList, Queue, PriorityQueue

Set -> HashSet, LinkedSet, TreeSet

Map -> HashMap

 
## List

```
list.size();

list.isEmpty();

list.contains(Object o);

 

list.add(int index, E element);

 

list.get(int index);

list.indexOf(Object o);

 

list.clear();

list.remove(int index);

list.remove(Object o);
```
 

 

### ArrayList

 
```
arraylist.clone();

arraylist.toArray();

arraylist.ensureCapacity(int mincapacity);  // 최소 사이즈 지정

arraylist.trimToSize();  // 사용하지 않는 부분 자르기
```
 

 

### LinkedList

 
```
linkedlist.clone();

linkedlist.toArray();

 

add(int index, E e) / addFirst() / addLast()

offer(E e) / offerFirst(E e) / offerLast(E e)

get(int index) / getFirst() / getLast()

peek() / peekFirst() / peekLast()  // 반환만

poll() / pollFirst() / pollLast()     // 제거하고 반환

```

 

### stack

 
```
push()

pop()

peek()
```
 

 

### Queue

 ```
isEmpty()

offer(E e)

peek()

poll()
```
 

 

### PriorityQueue

 
```
PriorityQueue pq = new PriorityQueue<>()

PriorityQueue pq = new PriorityQueue<>(new Collections.reverseOrder())

 

offer()

peek()

poll()
```
 
## Set / HashSet

 
```
set.size();

set.isEmpty();

set.contains(Object o);

 

set.add(int index, E element);

remove(Object o);
```
 

 

## Map / HashMap

 ```

map.clear()

map.size()

 

map.containsKey(Object key);

map.containsValue(Object value);

 

map.get(Object key);

map.getOrDefault(Object key, V defaultValue);

 

map.keySet();

map.values();

 

map.put(K key, V value);

 

map.remove();

map.replaec(K key, V value);
```
 

 
