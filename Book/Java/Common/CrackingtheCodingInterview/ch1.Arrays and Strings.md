# Chap 1. Arrays and Strings
### Hash Tables
1. hashcode를 계산 using hach code function
2. 계산 hashcode를 index에 맵핑
3. linked list에 value를 넣음. (collision 때문)
  - linked list 말고 collision에 대한 다른 알고리즘 있음 (찾아보기)

- collision이 심하면 O(N), where N is the number of keys. 하지만, collision을 피하는 알고리즘이기 때문에 대부분 O(1)임. index의 사이즈와 hash function에 따라...
- 메모리에 제약이 있을 겨우는 BST를 사용 O(log N)

### ArrayList & Resizable Arrays
O(1) Why??

### StringBuilder
String concatenation is O(xn^2). Why?

## Interview Questions
#### 1.1 Implement an algorithm to determine if a string has all unique characters. What if you cannot user additional data structure?
- Brute-Force
  - log(n^2)
- Using HashMap
  - log(n)

#### 1.2 **Check Permutation:** Given two strings, write a method to decide if one is a permutation of the other
- What is permutation?
https://www.khanacademy.org/math/precalculus/prob-comb/combinatorics-precalc/v/permutation-formula
- If each character and the count of each character is same, we can decide one is a permutation of the other
  - Using HashMap
    - 2 * log(n) right??
