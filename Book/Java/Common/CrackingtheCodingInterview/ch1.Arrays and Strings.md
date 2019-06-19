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
- Questions for Interviewer (by book)
  - if the string is an ASCII or Unicode
  - if it is ASCII, should ask if it is extended ASCII or not
- **Myself 1** Brute-Force (without data structure)
  - log(n^2)
- **Myself 2** Using HashMap (with data structure)
  - log(n)
- **Solution 1** by book. using boolean array of 128 or 256 (extended ASCII case) : **it's similar concept using HashMap** (Myself 2)
- **Solution 2** by book.  using int and shift operation (assumption that inputs are only lowercase)
- **Extra Suggestion 1** by book. Brute-Force way. It is same as 'Myself 1'
- **Extra Suggestion 2** by book. Sort and linear check




#### 1.2 **Check Permutation:** Given two strings, write a method to decide if one is a permutation of the other
- What is permutation?
https://www.khanacademy.org/math/precalculus/prob-comb/combinatorics-precalc/v/permutation-formula
- If each character and the count of each character is same, we can decide one is a permutation of the other
- Questions for Interviewer (by book)
  - permutation comparison is case sensitive
  - white space is significant
- **Myself 1** Using HashMap
    - 2 * log(n) right??
- **Solution 1** using sort
  - nlog(n)
- **Solution 2** using identical character count, int array of 128 (assumption it's ASCII ) : It's similar concept with using HashMap (counted) **  
