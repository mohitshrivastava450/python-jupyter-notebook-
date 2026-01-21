## 🔰 Introduction

Star patterns are visual designs created using the `*` character.  
They help beginners understand:
- Nested loops (`for` and `while`)
- Conditional statements
- Iterative logic

---

🌟 Examples of Star Patterns

1. Right-Angled Triangle

n=int(input("enter any number"))
for i in range(n):
    for j in range(i+1):
        print("*",end=" ")
    print()
    

enter any number 7

* 
* * 
* * * 
* * * * 
* * * * * 
* * * * * * 


2. Pyramid Pattern

n=int(input("enter any number"))
for i in range(n):
    for j in range(n-i-1):
        print(" ",end=" ")
    for j in range(2*i-1):
        print("*",end=" ")
    print()

enter any number 7

            
          * 
        * * * 
      * * * * * 
    * * * * * * * 
  * * * * * * * * * 
* * * * * * * * * * * 

3. Inverted Pyramid

n=int(input("enter any number"))
for i in range(n):
    for j in range(i):
        print(" ",end=" ")
    for j in range(n-1-i):
        print("*",end=" ")
    for j in range(n-i):
        print("*",end=" ")
    print()

enter any number 4

* * * * * * * 
  * * * * * 
    * * * 
      * 


4. Diamond Pattern

n=int(input("enter any number"))
for i in range(n-1):
    for j in range(n-i-1):
        print(" ",end=" ")
    for j in range(i+1):
        print("*",end=" ")
    for j in range(i):
        print("*",end=" ")
    print()
for k in range(n):
    for l in range(k):
        print(" ",end=" ")
    for l in range(n-1-k):
        print("*",end=" ")
    for l in range(n-k):
        print("*",end=" ")
    print()

enter any number 3

    * 
  * * * 
* * * * * 
  * * * 
    * 