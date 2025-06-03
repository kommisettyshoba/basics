BASICS:-
--------------------------
#1 to print even no.s
----------------------------
n=int(input("Enter n value:"))
for i in range(2,n,2):
    print(i,end=" ")
    
#2 to print odd no.s
--------------------------
n=int(input("Enter n value:"))
for i in range(1,n,2):
    print(i,end=" ")
#3
-----------
if 4:
    print("hello")
    if 3:
        print("hi")
#4
-------------
if 0:
    print("hello")
    if 3:
        print("hi")
#5
--------------------
for i in range(5): # 0 1 2 3 4 
    for j in range(5): #0 1 2 3 4 
        print(i,j,end=" ")
    print() #goes to new line i.e for i loop
#6
-----------------
n=1
print("even" if n%2==0 else "odd")

#7factorial
-----------------------
n=5
fact=1
for i in range(2,n+1):
    fact*=i
print(fact)

#8 o sum digits in a number
----------------------------------------
n = 123    #123%10=3 #123//10=2 #12//10=1 #1//10=0
sum=0
while n:
	sum+=n%10
	n//=10
print(sum)

#9 to find length
--------------------------
n=4595
count=0
while n:
	n//=10
	count+=1
print(count)

#10 armstrong
------------------------------
n=4595
count=0
temp=n
while n:
	n//=10
	count+=1
sum=0
n=temp
while n:
    single=n%10
    sum+=single**count
    n//=10
print("arm" if temp==sum else "not arm")

#11fib(to print particular Fibonacci number)
--------------------------------------------------------
n=6
if n<=1:
    print(n)
else:
    first=0
    second=1
    for i in range(n-1):
        third=first+second
        first=second
        second=third
print(third)

#12 palindrome
-----------------------------------
n=123
#123%10=3(res)
#123//10=12
#3*10=30+12%10=32
#32*10=320+1=321
n=12121
res=0
temp=n
while n:
    rem=n%10
    res=(res*10)+rem
    n//=10
print("palindrome" if res==temp else "not palindrome")

#13 prime or not
---------------------------------------
n=5
count=0
for i in range(1,n+1):
    if n%i==0:
        count+=1
print("prime" if count==2 else "not a prime")

#method-2:-
--------------
n=15
count=0
for i in range(2,n):
    if n%i==0:
        print("not a prime")
        break
else:
    print("prime")
    
#method-3:-
--------------
n=6
count=0
for i in range(2,n//2):
    if n%i==0:
        print("not a prime")
        break
else:
    print("prime")
    
#method-4:-
----------------------
n=6
count=0
for i in range(2,(n//2)+1):
    if n%i==0:
        print("not a prime")
        break
else:
    print("prime")
    
#14
--------------------------
r=20
for n in range(2,r+1):
    for i in range(2,(n//2)+1):
        if n%i==0:
            break
    else:
        print(n)
        
#15 to add even digits in a number
-----------------------------------------
n=98762
count=0
while n:
    rem=n%10
    if rem%2==0:
        count+=rem
    n=n//10
print(count)

#16 to add prime digits in a number
----------------------------------------
n=987464
count=0
while n:
    rem=n%10
    if rem in [2,3,5,7]:
        count+=rem
    n=n//10
print(count)

#Python programs using data types
#17 to print even no. in list
----------------------------------------
a=[1,2,3,4,5,6]
for i in a:
    if i%2==0:
        print(i)
        
#18 to print negative no. in list
------------------------------------------
a=[1,-2,3,-4,5,6]
for i in a:
    if i<0:
        print(i)
        
#19 to print reverse no. in list
---------------------------------------
a=[1,-2,3,-4,5,6]
for i in range(len(a)-1,-1,-1):
    print(a[i])
    
#20 to print reverse index in list
-----------------------------------------
a=[1,-2,3,-4,5,6]
for i in range(len(a)-1,-1,-1):
    print(i)
    
#21 to print odd no. in list
--------------------------------------
a=[1,-2,3,-4,5,6]
for i in range(0,len(a),2):
    print(a[i])
    
#22 to print even no. in list
------------------------------------
a=[1,-2,3,-4,5,6]
for i in range(1,len(a),2):
    print(a[i])
    
#23 moving zeros to last
-------------------------------
a=[1,2,0,3,0,4,5]
for i in a:
    if i==0:
        a.remove(0)
        a.append(0)
print(a)

#24 to print min no.
---------------------------------
a=[1,2,1,3,0,4,5]
search=a[0]
for i in range(1,len(a)):
    if search>a[i]:
        print(a[i])
        
#25 to print max no.
----------------------------------
a=[1,2,3,4,5,10]
search=a[0]
for i in range(1,len(a)):
    if a[i]<search:
        search=a[i]
print(a[i])

#26 to print min no.
-----------------------------
a=[1,0,2,3,4,5,10]
search=a[0]
for i in range(1,len(a)):
    if a[i]<search:
        search=a[i]
print(search)

#27 to delete duplicates
------------------------------
#method-1
.............
a=[1,0,2,3,3,4,5,10]
print(set(a))

#method-2
................
a=[1,0,2,3,3,4,5,10]
res=[] #to create empty list
for i in a:
    if i not in res:
        res.append(i)
print(res)

#28 to count no. of times a value is present
--------------------------------------------------
a=[1,3,2,5,3,2,2]
res={} #to create empty dictionary
for i in a:
    if i in res:
        res[i]+=1
    else:
        res[i]=1
print(res)

#29 to sum of postive and negative values
-------------------------------------------------
a=[1,3,2,-5,-4]
pos=0
neg=0
for i in a:
    if i>0:
        pos+=i
    else:
        neg+=i
print([pos,-neg])

#30 to remove vowels
-------------------------------
a="abijoajk"
res=" "
for i in a:
    if i not in "aeiou":
        res+=i
print(res)

#31 to print only vowels
------------------------------------
a="abijoajk"
res=" "
for i in a:
    if i in "aeiou":
        res+=i
print(res)

#ORD: ord converts alphabet into ascii..................
#CHR: chr converts ascii into alphabet..................
#32 
-----------------
a="aikhofj"
res=""
for i in a:
    if i in "aeiou":
        res+=chr(ord(i)-32)
    else:
        res+=i
print(res)

#33 to print the addition of range of alphabets
--------------------------------------------------
a="abc"
res=0
for i in a:
    res+=ord(i)-96
print(res)

#34 to print 1 to n using while
--------------------------------------
n=int(input())
i=1
while i<=n:
    print(i)
    i+=1
    
#35 to print n to 0
-------------------------------
n=10
for i in range(n+1,0,-1):
    print(i)
    
#36 print only single digit
---------------------------------
li=[1,12,3,24,5,53]
for i in li:
    if i<10:
        print(i)
        
#37 add only single digit
----------------------------------
li=[1,12,3,24,5,53]
count=0
for i in li:
    if i<10:
        count+=i
print(count)

#38 to print a number if sum of that number and its index is even
-------------------------------------------------------------------
l=[1,3,2,4]
for i in range(len(l)):
    sum= l[i]+i
    if sum%2==0:
        print(l[i])
        
#39 to print only capital letters
-------------------------------------------
l="aAbBcC"
for i in l:
    if ord(i)>=65 and ord(i)<97:
        print(i)
        
#40 to print only small letters
---------------------------------------
l="aAbBcC"
for i in l:
    if ord(i)>=97 and ord(i)<=122:
        print(i)
        
#41 to print only digits
---------------------------------------------
a="jk78687jrt"
for i in a:
    if ord(i) in range(48,58):
        print(i)
        
#42 to print only alphabets
-----------------------------------------
a="ghj437688"
for i in a:
    if ord(i) in range(65,91) or ord(i) in range(97,123):
        print(i)
        
#43 sum of odd index values and even index values
---------------------------------------------------------
a=[1,2,3,4,5,6]
odd_sum=0
even_sum=0
for i in range(len(a)):
    if a[i]%2==0:
        even_sum+=a[i]
    else:
        odd_sum+=a[i]
print(even_sum)
print(odd_sum)
if even_sum>odd_sum:
    print("even")
else:
    print("Odd")
    
#44 to print present index+next index value
--------------------------------------------------
a=[1,2,3,1,5]
start=0
while start<len(a):
    print(a[start])
    start=start+a[start]
    
#45 to sum until it is single digit
------------------------------------------
n=12345
while n>=10:
    sum=0
    while n:
        sum+=n%10
        n//=10
    n=sum
print(n)

#46 to print digits and alp separately
--------------------------------------------
a="nbjh6678nbj"
num=alp=""
for i in a:
    if ord(i) in range(48,58):
        num+=i
    else:
        alp+=i
print(num,alp)

#47 to check n is in the table of a
------------------------------------------
n=int(input())
a=int(input())
if n%a==0:
    print(f"{n} is in the table of {a}")
else:
    print(f"{n} is not in the table of {a}")
    
#48 from 0th index increaing value count n=1234557 and return output as 5
-------------------------------------------------------------------------------
n=12343
n=str(n)
prev=0
for i in range(len(n)):
    if prev>=int(n[i]):
        break
    prev=int(n[i]) 
else:
    i+=1
print(i)

#49 to print rank
--------------------------------
a=2
b=3
c=1
if a>b and a>c:
    if b>c:
        print("a1 b2 c3")
    else:
        print("a1 c2 b3")
elif b>c:
    if a>c:
        print("b1 a2 c3")
    else:
        print("b1 c2 a3")
else:
    if a>b:
        print("c1 a2 b3")
    else:
        print("c1 b2 a3")
        
#50 missing sequence
-------------------------------------
a=[1,2,3,4,5]
b=[1,2,4,5]
for i in range(len(b)):
    if a[i]!=b[i]:
        print(i)
        break
else:
    print(i+1)
    
#51 to return even in sorted and odd in any order
--------------------------------------------------------
even=[]
odd=[]
for i in a:
    if i%2==0:
        even.append(i)
    else:
        odd.append(i)
for i in range(len(even)):
    for j in range(len(even)-1):
                if even[j]>even[j+1]:
                    even[j],even[j+1]=even[j+1],even[j]
result=even+odd
print(result)

#52 sum of other two elements
--------------------------------------
a=[1,2,3]
res=[a[1]+a[2],a[0]+a[2],a[0]+a[1]]
print(res)

#53 to check password is valid or not
----------------------------------------------
def verification(a):
    alp=dig=sym=up=lo=False
    if not (8<=len(a)<=10):
        return False
    for i in a:
        if i.isalpha():
            if i.isupper():
                up=True
            else:
                lo=True 
        if i.isdigit():
            dig=True
        if i in "@_":
            sym=True
    if sym and dig and up and lo:
        return True
    return False           
a=input()
print(verification(a))

#54 pan verification
--------------------------------
pan=input()
print(len(pan)==10 and pan[:5].isalpha() and pan[:5].isupper() and pan[5:-1].isdigit() and pan[-1].isalpha() and pan[-1].isupper())
---------------------------------------------------------------
#STACK:-
.......................
#1
----------------
class stack:
    def __init__(self,size):
        self.size = size
        self.box = [0]*self.size
        self.top = -1
    def push(self,data):
        if self.top+1 == self.size:
            print("overflow")
            return
        self.top+=1
        self.box[ self.top ] = data
    def display(self):
        if self.top == -1:
            print("underflow")
            return
        for i in range(self.top,-1,-1):
            print(self.box[i],end=" ")
    def pop(self):
        if self.top == -1:
            print("underflow")
            return
        self.top-=1
    def peek(self):
        if self.top == -1:
            print("underflow")
            return
        print(self.box[self.top])
stack1 = stack(3)
stack1.push(18)
stack1.push(7)
stack1.display()
stack1.pop()
stack1.pop()
print()
stack1.display()

#2
--------------------------------
class stack:
    def __init__(self):
        self.box = []
    def push(self,data):
        self.box.append(data)
    def display(self):
        if len(self.box)==0:
            print("empty")
            return
        for i in self.box[::-1]:
            print(i,end=" ")
    def pop(self):
        if len(self.box) == 0:
            print("empty")
            return
        self.box.pop()
    def peek(self):
        if len(self.box) == 0:
            print("empty")
            return
        print(self.box[-1])
stack1 = stack()
stack1.push(18)
stack1.push(7)
stack1.display()
stack1.pop()
stack1.pop()
print()
stack1.display()

#3 QUEUE:
---------------------------------------
class Queue:
    def __init__(self):
        self.queue = []
    def enqueue(self,data):
        self.queue.append(data)
    def display(self):
        if len(self.queue)==0:
            print("empty")
            return
        for i in self.queue:
            print(i,end=" ")
    def dequeue(self):
        if len(self.queue) == 0:
            print("empty")
            return
        self.queue.pop(0)
    def front(self):
        if len(self.queue) == 0:
            print("empty")
            return
        print(self.queue[0])
obj = Queue()
obj.enqueue(18)
obj.enqueue(7)
obj.display()
obj.dequeue()
print()
obj.display()

#4 DOUBLE-ENDED QUEUE:
-------------------------------------
class Queue:
    def __init__(self,size):
        self.size = size
        self.front=self.rear = -1
        self.queue = [0]*self.size
    def enqueue(self,data):
        if self.rear == -1:
            self.front=self.rear=0
            self.queue[self.rear]=data
            return
        if self.rear+1 == self.size:
            print("is_full")
            return
        self.rear+=1
        self.queue[self.rear] = data
    def display(self):
        if self.front == -1 or self.front > self.rear:
            print("empty")
            return
        for i in range(self.front , self.rear+1):
            print(self.queue[i],end=" ")
    def dequeue(self):
        if self.front ==-1 or self.front>self.rear:
            print("empty")
            return
        self.front+=1
    def front1(self):
        if self.front == -1 or self.front > self.rear:
            print("empty")
            return
        print(self.queue[self.front])
obj = Queue(3)
obj.enqueue(18)
obj.enqueue(7)
obj.display()
obj.dequeue()
print()
obj.display()

#5 LINKED-LIST:
-------------------------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.next = None
class Linked_list:
    def __init__(self):
        self.head=None
    def b_insert(self,data):
        newnode = Node(data)
        newnode.next = self.head
        self.head = newnode
    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = newnode
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next
obj = Linked_list()
obj.b_insert(8)
obj.b_insert(10)
obj.b_insert(21)
obj.e_insert(36)
obj.display()

#6 LinkedList
-------------------------------
class Node:
    def _init_(self,data):
        self.data=data
        self.next = None
class Linked_list:
    def _init_(self):
        self.head=None
    def b_insert(self,data):
        newnode = Node(data)
        newnode.next = self.head
        self.head = newnode
    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = newnode
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next
    def e_delete(self):
        if self.head is None or self.head.next==None:
            self.head=None
            return
        cur=self.head
        while  cur.next.next:
            cur=cur.next
        cur.next=None
        
obj = Linked_list()
obj.b_insert(8)
obj.b_insert(10)
obj.b_insert(21)
obj.e_insert(36)
obj.e_delete()
obj.e_delete()
obj.e_delete()
obj.display()

#7 LinkedList deletion at begin
----------------------------------------------
class Node:
    def _init_(self,data):
        self.data=data
        self.next = None
class Linked_list:
    def _init_(self):
        self.head=None
    def b_insert(self,data):
        newnode = Node(data)
        newnode.next = self.head
        self.head = newnode
    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = newnode
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next
    def e_delete(self):
        if self.head is None or self.head.next==None:
            self.head=None
            return
        cur=self.head
        while  cur.next.next:
            cur=cur.next
        cur.next=None
    def b_delete(self):
        if self.head:
            self.head=self.head.next      
obj = Linked_list()
obj.b_insert(8)
obj.b_insert(10)
obj.e_insert(36)
obj.display()
print()
obj.b_delete()
obj.display()

#8
--------------------------
class Node:
    def __init__(self,data):
        self.data = data
        self.next = None
        self.prev = None

class Double_linkedlist:
    def __init__(self):
        self.head=self.tail=None

    def b_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head =self.tail= newnode
            return
        newnode.next = self.head
        self.head.prev = newnode
        self.head = newnode

    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head =self.tail= newnode
            return
        newnode.prev = self.tail
        self.tail.next = newnode
        self.tail = newnode

    def forward_display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next

    def backward_display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.tail
        while cur:
            print(cur.data, end="->")
            cur = cur.prev
    def b_delete(self):
        if self.head == self.tail:
            self.head = self.tail =None
        if self.head:
            self.head = self.head.next
            self.head.prev=None

    def e_delete(self):
        if self.head == self.tail:
            self.head = self.tail =None
        if self.tail:
            self.tail = self.tail.prev
            self.tail.next = None

    def position(self,pos):
        cur = self.head
        for i in range(pos-1):
            if cur.next is None:
                break
            cur = cur.next
        else: return cur


    def position_insert(self,data,pos):
        if pos == 1:
            self.b_insert(data)
            return
        cur = self.position(pos)
        # if cur == self.tail:
        #     self.e_insert(data)
        #     return
        newnode = Node(data)
        if cur:
            newnode.next = cur
            newnode.prev = cur.prev
            cur.prev = newnode.prev.next = newnode

    def position_delete(self, pos):
        if pos == 1:
            self.b_delete()
            return
        cur = self.position(pos)
        if cur == self.tail:
            self.e_delete()
            return
        if cur:
            cur.next.prev = cur.prev
            cur.prev.next = cur.next
            cur.prev=cur.next=None


obj = Double_linkedlist()
obj.e_insert(6)
obj.e_insert(10)
obj.e_insert(30)
obj.b_insert(5)
obj.forward_display()
print()
obj.backward_display()
obj.position_delete(2)
print()
obj.forward_display()
print()
obj.backward_display()

#9
-------------------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.next = None



class Linked_list:
    def __init__(self):
        self.head=None

    def b_insert(self,data):
        newnode = Node(data)
        newnode.next = self.head
        self.head = newnode

    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = newnode


    def e_delete(self):
        if self.head is None or self.head.next is None:
            self.head = None
            return
        cur = self.head
        while cur.next.next:
            cur = cur.next
        cur.next = None


    def b_delete(self):
        if self.head:
            self.head = self.head.next

    def pos_delete(self,pos):
        if pos == 1:
            self.b_delete()
            return
        cur = self.position(pos - 1)
        if cur and cur.next:
            cur.next = cur.next.next
        else:
            print("position not found")


    def position(self,pos):
        if pos<=0:
            print("invalid position")
            return

        cur = self.head
        for i in range(pos-1):
            if cur.next==None:
                break
            cur = cur.next
        else: return cur
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next

    def pos_insert(self,data,pos):
        if pos == 1:
            self.b_insert(data)
            return
        newnode = Node(data)
        cur = self.position(pos-1)
        if cur:
            newnode.next = cur.next
            cur.next = newnode
        else: print("position not found")

obj = Linked_list()
obj.b_insert(10)
obj.e_insert(8)
obj.e_insert(36)
obj.display()
print()
obj.pos_delete(4)
obj.display()

#10
----------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.next = None

class Linked_list:
    def __init__(self):
        self.head=None

    def b_insert(self,data):
        newnode = Node(data)
        newnode.next = self.head
        self.head = newnode

    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = newnode


    def e_delete(self):
        if self.head is None or self.head.next is None:
            self.head = None
            return
        cur = self.head
        while cur.next.next:
            cur = cur.next
        cur.next = None


    def b_delete(self):
        if self.head:
            self.head = self.head.next

    def position(self,pos):
        if pos<=0:
            print("invalid position")
            return
        cur = self.head
        for i in range(pos-1):
            if cur.next==None:
                break
            cur = cur.next
        else: return cur
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next

    def pos_insert(self,data,pos):
        if pos == 1:
            self.b_insert(data)
            return
        newnode = Node(data)
        cur = self.position(pos-1)
        if cur:
            newnode.next = cur.next
            cur.next = newnode
        else: print("position not found")

obj = Linked_list()

obj.b_insert(10)
obj.e_insert(8)
obj.e_insert(36)
obj.display()
print()
obj.pos_insert(17,4)
obj.display()

#11
-----------------------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.next = None
class Linked_list:
    def __init__(self):
        self.head=None

    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
            cur = cur.next
        cur.next = newnode
    def remove_dup(self):
        cur = self.head
        while cur and cur.next:
            if cur.data == cur.next.data:
                cur.next = cur.next.next
            cur = cur.next
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next
t = int(input())
obj= [0]*t
for i in range(t):
    obj[i] = Linked_list()
    n = int(input())
    a = list(map(int,input().split(" ")))
    for j in range(n):
        obj[i].e_insert(a[j])
    obj[i].remove_dup()
for k in obj:
    k.display()
    print()
    
#TREE:
.................................
#12 inorder traversal
---------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.left=self.right=None
def inorder_traversal(root):
    if root is None:
        return
    inorder_traversal(root.left)
    print(root.data)
    inorder_traversal(root.right)
root=Node(5)
root.left=Node(6)
root.right=Node(12)
root.left.left=Node(10)
root.left.right=Node(33)
root.left.left.left=Node(56)
root.right.right=Node(3)
inorder_traversal(root)

#13 preorder traversal
---------------------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.left=self.right=None
def inorder_traversal(root):
    if root is None:
        return
    print(root.data)
    inorder_traversal(root.left)
    inorder_traversal(root.right)
root=Node(5)
root.left=Node(6)
root.right=Node(12)
root.left.left=Node(10)
root.left.right=Node(33)
root.left.left.left=Node(56)
root.right.right=Node(3)
inorder_traversal(root)

#14 postorder traversal
---------------------------------------------
class Node:
    def __init__(self,data):
        self.data=data
        self.left=self.right=None
def inorder_traversal(root):
    if root is None:
        return
    inorder_traversal(root.left)
    inorder_traversal(root.right)
    print(root.data)
root=Node(5)
root.left=Node(6)
root.right=Node(12)
root.left.left=Node(10)
root.left.right=Node(33)
root.left.left.left=Node(56)
root.right.right=Node(3)
inorder_traversal(root)

#15 
-----------------------------
class Node:
    def __init__(self,data):
        self.data=data     #data for the node 
        self.left=None     #value stored in left side
        self.right=None    #value stored in right side
        
class binary_tree:  #new class created
    
        
    def inorder_traversal(self,root):
        if root is None:
            return
        self.inorder_traversal(root.left)
        print(root.data,end=" ")
        self.inorder_traversal(root.right)

    def height(self,root):  #finding height of the tree
        if root is None or root.left is None and root.right is None:
            return 0
        l_count=1+self.height(root.left)
        r_count=1+self.height(root.right)
        return l_count if l_count>r_count else r_count    

root=Node(5)
root.left=Node(6)
root.right=Node(12)
root.right.right=Node(3)
root.left.left=Node(10)
root.left.right=Node(33)
root.left.left.left=Node(56)
obj=binary_tree()
obj.inorder_traversal(root)
print()
print(obj.height(root))

#16
-------------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None
class bst:
    def __init__(self):
        self.root = None
    def insert(self,data):
        self.root = self.rec_insert(self.root,data)
    def rec_insert(self,root,data):
        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root
    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)
obj = bst()
obj.insert(25)
obj.insert(63)
obj.insert(72)
obj.insert(22)
obj.insert(35)
obj.insert(17)
obj.inorder()

#17 height of bst
-------------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None
class bst:
    def __init__(self):
        self.root = None
    def insert(self,data):
        self.root = self.rec_insert(self.root,data)
    def rec_insert(self,root,data):
        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root
    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)
    def count(self,root):
        if not root:
            return 0
        return 1+self.count(root.left)+self.count(root.right)
obj = bst()
obj.insert(25)
obj.insert(63)
obj.insert(72)
obj.insert(22)
obj.insert(35)
obj.insert(17)
obj.inorder()
print(obj.count(obj.root))

#18 height of tree by using max func
--------------------------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None
class bst:
    def __init__(self):
        self.root = None
    def insert(self,data):
        self.root = self.rec_insert(self.root,data)
    def rec_insert(self,root,data):
        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root
    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)
    def count(self,root):
        if not root:
            return 0
        return 1+max(self.count(root.left),self.count(root.right))
obj = bst()
obj.insert(25)
obj.insert(63)
obj.insert(72)
obj.insert(22)
obj.insert(35)
obj.insert(17)
obj.inorder()
print()
print(obj.count(obj.root))

#19 sum of all values
-------------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None
class bst:
    def __init__(self):
        self.root = None
    def insert(self,data):
        self.root = self.rec_insert(self.root,data)
    def rec_insert(self,root,data):
        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root
    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)
    def count(self,root):
        if not root:
            return 0
        return 1+max(self.count(root.left),self.count(root.right))
    def sum(self,root):
        if not root:
            return 0
        return root.data+self.sum(root.left)+self.sum(root.right)
obj = bst()
obj.insert(25)
obj.insert(63)
obj.insert(72)
obj.insert(22)
obj.insert(35)
obj.insert(17)
obj.inorder()
print()
print(obj.count(obj.root))
print(obj.sum(obj.root))

#20 ALL MIX
---------------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None
class bst:
    def __init__(self):
        self.root = None
    def insert(self,data):
        self.root = self.rec_insert(self.root,data)
    def rec_insert(self,root,data):
        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root
    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)
    def sum(self,root):
        if not root:  return 0
        return root.data + self.sum(root.left) + self.sum(root.right)
    def count(self, root):
        if not root:  return 0
        return 1 + self.count(root.left) + self.count(root.right)
    def height(self, root):
        if not root:  return 0
        return 1 + max(self.height(root.left) , self.height(root.right))
obj = bst()
obj.insert(20)
obj.insert(60)
obj.insert(70)
obj.insert(25)
obj.insert(35)
obj.insert(10)
obj.inorder()
print()
print( obj.sum(obj.root) )
print( obj.count(obj.root) )
print( obj.height(obj.root)-1 )

#21 COUNT, MIN AND MAX
---------------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None
class bst:
    def __init__(self):
        self.root = None
    def insert(self,data):
        self.root = self.rec_insert(self.root,data)
    def rec_insert(self,root,data):
        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root
    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)
    def sum(self,root):
        if not root:  return 0
        return root.data + self.sum(root.left) + self.sum(root.right)
    def count(self, root):
        if not root:  return 0
        return 1 + self.count(root.left) + self.count(root.right)
    def height(self, root):
        if not root:  return 0
        return 1 + max(self.height(root.left) , self.height(root.right))
    def left_sum(self,root):
        if not root:
            return 0
        self.left_sum(root.right)
        left =   self.left_sum(root.left)
    def min(self,root):
        if root is None:
            print("no data")
        while root.left:
            root = root.left
        return root.data
    def max(self, root):
        if root is None:
            print("no data")
        while root.right:
            root = root.right
        return root.data
obj = bst()
obj.insert(20)
obj.insert(60)
obj.insert(70)
obj.insert(5)
obj.insert(351)
obj.insert(10)
obj.inorder()
print()
print( obj.max(obj.root) )

#Deletion in bst:------------------
#left side biggest child:------------
#right side smallest child:------------------  
#deletion:--------------------
#22
---------------------------
def find(self,root,key):
    if root is None or root.data==key:
        return root
    if key<root.data:
        return self.find(root.left,key)
    else:
        return self.find(root.right,key)
def delete(self,root,key):
    if root:
        if root.data > key:
            root.left=self.delete(root.left,key)
            return root 
        elif root.data<key:
            root.right=self.delete(root.right,key)
            return root
        if root.left is None:
            return root.right 
        elif root.right is None:
            return root.left
        max_val=self.max(root.left) #from max function
        root.data=max_val
        self.delete(root.left,max_val)
        return root
obj.delete(obj.root,25)

#23 DELETION OF BST
--------------------------------------
class Node:
    def __init__(self,data):
        self.data =data
        self.left=None
        self.right=None

class bst:
    def __init__(self):
        self.root = None

    def insert(self,data):
        self.root = self.rec_insert(self.root,data)

    def rec_insert(self,root,data):

        if root is None:
            return Node(data)
        if root.data >data:
            root.left = self.rec_insert(root.left,data)
        else:
            root.right = self.rec_insert(root.right,data)
        return root

    def inorder(self):
        def rec_inorder(root):
            if root:
                rec_inorder(root.left)
                print(root.data,end=" ")
                rec_inorder(root.right)
        rec_inorder(self.root)

    def sum(self,root):
        if not root:  return 0
        return root.data + self.sum(root.left) + self.sum(root.right)

    def count(self, root):
        if not root:  return 0
        return 1 + self.count(root.left) + self.count(root.right)

    def height(self, root):
        if not root:  return 0
        return 1 + max(self.height(root.left) , self.height(root.right))

    # def left_sum(self,root):
    #     if not root:
    #         return 0
    #     self.left_sum(root.right)
    #     left =   self.left_sum(root.left)
    #     return left

    def left_sum(self,root):
        if root is None:
            return 0
        total = 0
        if root.left:
            total += root.left.data
        total += self.left_sum(root.left)
        total += self.left_sum(root.right)
        return total

    def right_sum(self,root):
        if root is None:
            return 0
        rightsum= self.sum(root) - self.root.data - self.left_sum(root)
        return rightsum

    def min(self,root):
        if root is None:
            print("no data")
        while root.left:
            root = root.left
        return root.data

    def max(self, root):
        if root is None:
            print("no data")
        while root.right:
            root = root.right
        return root.data

    def find(self,root,key):
        if root is None or root.data == key:
            return root
        if key < root.data:
            return self.find(root.left,key)
        else:
            return self.find(root.right,key)

    def delete(self,key):
        self.root = self.rec_delete(self.root,key)
    def rec_delete(self,root,key):
        if root:
            if root.data > key:
                root.left = self.rec_delete(root.left,key)
            elif root.data < key:
                root.right = self.rec_delete(root.right,key)
            else:
                if root.left is None:
                    return root.right
                elif root.right is None:
                    return root.left
    
                max_val = self.max(root.left)
                root.data = max_val
                self.rec_delete(root.left,max_val)
            return root
            
#24 graphs-Adjacent List
----------------------------------------------------
class Graph:
    def __init__(self):
        self.graph={}
    def insert(self,v,e):
        if v not in self.graph:
            self.graph[v]=[e]
        else:
            self.graph[v].append(e)
obj=Graph()
obj.insert("B","T") #from B to T
obj.insert("T","B")
obj.insert("B","P")
obj.insert("P","B")
obj.insert("D","P")
obj.insert("P","D")
obj.insert("D","T")
obj.insert("T","D")
obj.insert("B","L")
obj.insert("L","B")
print(obj.graph)

#25 ADJACENCY MATRIX
---------------------------------------------
class Graph:
    def __init__(self,size):
        self.graph = [ [0]*size for i in range(size)]
        self.dict = {"B": 0, "T": 1, "P": 2, "D": 3, "L": 4}
    def insert_list(self,v,e):
        if v not in self.graph:
            self.graph[v] = [e]
        else:
            self.graph[v].append(e)

    def insert_matrix(self,v,e):
        row , col = self.dict[v] ,self.dict[e]
        self.graph[row][col]=1
        self.graph[col][row]=1
obj = Graph(5)
obj.insert_matrix("B","T")
obj.insert_matrix("B","P")
obj.insert_matrix("B","L")
obj.insert_matrix("D","P")
obj.insert_matrix("D","T")
print(obj.graph)

#26 BFS:We use queue
----------------------------------------------
class Graph:
    def __init__(self,size):
            self.graph = {}
    def insert_list(self,v,e):
        if v not in self.graph:
            self.graph[v] = [e]
        else:
            self.graph[v].append(e)

    def bfs(self,start):
        queue = [start]
        visited = []
        while queue:
            cur = queue.pop(0) #if 0 it is bfs, without 0 dfs
            if cur not in visited:
                visited.append(cur)
                queue.extend(self.graph[cur])
        print(visited)
obj = Graph()
obj.insert_list("B","T")
obj.insert_list("T","B")
obj.insert_list("B","P")
obj.insert_list("P","B")
obj.insert_list("B","D")
obj.insert_list("D","B")
obj.insert_list("P","D")
obj.insert_list("D","P")
obj.insert_list("T","D")
obj.insert_list("D","T")
obj.insert_list("D","G")
obj.insert_list("G","D")
obj.insert_list("D","K")
obj.insert_list("K","D")
obj.insert_list("K","L")
obj.insert_list("L","K")
print(obj.graph)
obj.bfs("B")

#27 Linear search:one by one. it searches sequentially.
-----------------------------------------------------------------
def linear_search(a,key):
    for i in range(len(a)):
        if a[i]==key:
            return f"{key} found in the index of {i}"
    return "not found"
a=[4,6,7,420,3,20,41,81]
print(linear_search(a,420))
print(linear_search(a,5))

#28 Binary search:take mid value. it works only for sorted list.(not sequentially)
------------------------------------------------------------------------------------------------
def binary_search(a,key):
    s=0
    e=len(a)-1
    while s<=e: #checks until start crosses end
        mid=(s+e)//2
        if a[mid]==key: #a[mid] means it takes value of that index =12(3rd index)
            return mid
        elif a[mid]>key:
            e=mid-1
        else:
            s=mid+1
        
a=[5,8,10,12,41,45,81,108]
print(binary_search(a,8))

# Sorting:arranging the elements in sequence order i.e., asc or des order.
------------------------------------------------------------------------------------
#29 Bubble sort:bubble values goes to the top.It takes n-1 iterations.
-------------------------------------------------------------------------------
def bubble_sort(a):
    for phase in range(1,len(a)):
        #phase 1 
        for i in range(len(a)-phase): #here phase=1 so 6-1=5 
            if a[i]>a[i+1]:
                a[i],a[i+1]=a[i+1],a[i]
    return a         
a=[21,18,61,45,81,10]
print(bubble_sort(a))

#30 bubble_sort
------------------------------
def bubble_sort(a):
    for phase in range(1,len(a)):
        flag=0
        #phase 1 
        for i in range(len(a)-phase): #here phase=1 so 6-1=5 
            if a[i]>a[i+1]:
                flag=1
                a[i],a[i+1]=a[i+1],a[i]
        if flag==0: #if flag remains zero then stop program and got to for loop phase
            break
    return a
a=[21,18,61,45,81,10]
print(bubble_sort(a))

#31 selection_sort
-------------------------------------
def selection_sort(a):
    for phase in range(len(a)-1):
        min=phase
        #phase 1 
        for i in range(phase+1,len(a)): 
            if a[i]<a[min]:
                min=i
        if min!=phase: 
            a[min],a[phase]=a[phase],a[min]
    return a
a=[21,18,61,45,81,10]
print(selection_sort(a))

#32 insertion_sort
-------------------------------------------
def insertion_sort(a):
    for i in range(1,len(a)):
        j=i-1
        temp=a[i] #stores the copy of values of ith position
        while j>=0 and a[j]>temp:
            a[j+1]=a[j]
            j-=1 
        a[j+1]=temp
    return a
a=[21,18,61,45,81,10]
print(insertion_sort(a))

#33 quick_sort
--------------------------------------------------
def quick_sort(a,s,e):
    if s<e:
        pivot_index = partition(a,s,e)
        quick_sort(a,s,pivot_index-1)
        quick_sort(a,pivot_index+1,e)
def partition(a,s,e):
    pivot = e
    l = e-1
    while s<=l:
        while a[s] < a[pivot]:
            s+=1
        while l>=0 and a[l]>= a[pivot]:
            l-=1
        if s<l: a[s] , a[l]  = a[l] ,a[s]
    if s>l:  a[s] , a[pivot] = a[pivot] , a[s]
    return s
a = [ 21 ,18,61,45,81,10]
print( quick_sort(a,0,len(a)-1) )
print(a)	

#34
---------------------------------------------
def Merge_sort(arr):
    if len(arr)==1:
         return
    mid = len(arr)//2
    left = arr[:mid]
    right = arr[mid:]
    Merge_sort(left)
    Merge_sort(right)

    k = i= j =0
    while i<len(left) and j<len(right):
        if left[i]<right[j]:
            arr[k] = left[i]
            i+=1
        else:
            arr[k] = right[j]
            j+=1
        k+=1
    while i<len(left):
        arr[k]=left[i]
        i+=1
        k+=1
    while j < len(right):
        arr[k] = right[j]
        j+=1
        k+=1
a = [ 21 ,18,61,45,81,10]
Merge_sort(a)
print(a)
----------------------------------------
oops
--------------------------------
#Functions programs in python
#1
--------------------------
def sree(a,b):#with argument without return type
    print(a+b)
sree(15,20)
sree(5,20)

#2
----------------------
def sree(a,b):#with argument without return type
    return a+b
print(sree(15,20))
print(sree(5,20))

#3
--------------------------
a=lambda x,y:x+y
print(a(1,9))

#4 generator func
-----------------------------
def fun(n):
    i=0
    while i<n:
        yield i
        i+=1
print(list(fun(5)))

#5 Decorator func:that modify (or) extend behavior of other function.
---------------------------------------------------------------------------
def my_dec(func):
    def wrapper():
        print("a")
        func()
        print("ab")
    return wrapper
@my_dec
def say_hello():
    print("Hi")
say_hello() 

#6
---------------------------------
def my_dec(a):
    def b():
        a()
        print("ab")
        print("abd")
    return b
@my_dec
def say_hello():
    print("Hi")
say_hello() 

#7 closure: that captures and remember the values in the enclosing scope even if they are not present in memory.
--------------------------------------------------------------------------------------------------------
def outer_function(x):
    def inner_function(y):
        return x+y
    return inner_function
closure=outer_function(10)
print(closure(5))

#Built-in functions: python standard library
#8
-------------------------------------------
a="7skjdbf"
print(a[0].isalpha())

#9
-----
a="79984375"
print(a.count("9"))

#10
-------------------
a="HGFHGJ"
print(a.lower())

#11
-----------------------
a="HGFHGJ"
print(a.replace("H","k"))

#12
------------------------
a="HGFHGJ"
for i, e in enumerate(a):
    print(i,e)
    
#Recursive functions: Functions that call themselves, either directly or indirectly.
#13
-------------------------------------------------------------------
def a():
    print("sd")
    a()
a()

#14
-------------------------------
def a(n):
    if n==1:
        return
    print(n)
    a(n-1)
a(5)
    
#15
---------------------------------
def a(n):
    print(n)
    if n==1:
        return
    a(n-1)
a(5)

#16
----------------------------------
def a(n):
    if n==1:
        return
    a(n-1)
    print(n)
a(5)

#17
----------------------------
def a(n):
    if n==1:
        return
    print(n)
    a(n-1)
    print(n)
a(5)

#18
----------------------------------
def a(n):
    if n==1:
        return
    a(n-1)
    print(n)
    a(n-1)
a(3)

#19
------------------------------
def sree(a,b):#parameters
    print(a,b)
sree(10,20)#arguments

#20
---------------------------
def sree(a,b=0):
    print(a,b)
sree(10)

#21
---------------------------
def sree(a,b=0):
    print(a,b)
sree(10,8)

#23
---------------------------
def sree(b=3):
    print(b)
sree()

#24
----------------------------
def sree(a,b=3,c=0,d=0,e=0):
    print(a,b,c)
sree(2,4)

#25
-----------------------------
def sree(*a):
    print(a)
sree(2,6.7,"hi")
def sree(*a):
    a=list(a)
    print(a)
sree(2,6.7,"hi")

#26 Arbitrary keyword:
----------------------------------
def sree(**a):
    print(a)
sree(rank=1,age=20,roll=21,name="lakshmi")

#27
---------------------------------
def sum(n):
    if n==1:
        return 1
    return n+sum(n-1)
print(sum(5))

#28 fibonnace
------------------------------
def sum(n):
    if n==1:
        return 1
    return n*sum(n-1)
print(sum(5))

#29 sum of given integer
------------------------------
def sum(n):
    if n<10:
        return n
    return n%10+sum(n//10)
print(sum(123))

#30 finding min in given list
------------------------------------
def sum(n,i=0):
    if i==len(n)-1:
        return n[i]
    return min(n[i],sum(n,i+1))    
l=[2,3,6,1,5]
print(sum(l))

#method-2
...............
def sum(n,i=0):
    if i==len(n)-1:
        return n[i]
    min=sum(n,i+1)
    return n[i] if n[i]<min else min  
l=[2,3,6,5]
print(sum(l))

#OOPS
---------------
#31. class & object:
--------------------
class com_lab:
    bench=2
    dustbin=1
vin=com_lab() #vin is member of class
print(vin.bench)

#32
-----------------------
class com_lab:
    bench=2
    dustbin=1
vin=com_lab()
sid=com_lab()
gin=com_lab()
print(vin.bench, sid.bench)

#33
---------------------
class com_lab:
    bench=2
    dustbin=1
    def projector():
        print("on")
vin=com_lab()
sid=com_lab()
gin=com_lab()
com_lab.projector() #only com_lab has access but not vin, sid, gin.

#34 Instance Method:
---------------------------------
class com_lab:
    bench=2
    dustbin=1
    def system(self):
        print("System")
    def projector():
        print("on")
vin=com_lab()
sid=com_lab()
gin=com_lab()
gin.system() #this is not accessed by class.

#35 (or)
-----------------
class com_lab:
    bench=2
    dustbin=1
    def system(self):
        print("System")
    def projector():
        print("on")
vin=com_lab()
sid=com_lab()
gin=com_lab()
com_lab.system(gin)

#36 constructor
------------------------
class com_lab:
    bench=2
    dustbin=1
    def __init__(self): #constructor
        print("Welcome")
    def system(self):
        print("System")
    def projector():
        print("on")
gin=com_lab()
gin.system()

#37 Instance attribute:
--------------------------------
class com_lab:
    def __init__(self,amt):
        self.amt=amt
    def return_back(self):
        return self.amt
gin=com_lab(10)
vin=com_lab(20)
sin=com_lab(30)
print(sin.return_back())

#Inheritance:Inheriting the properties and behavior from the parent class.
#38
-------------------------------------------------------------------------------
class com_lab_a:
    gin=56
class com_lab_b(com_lab_a):
    sin_amt=80
sin=com_lab_b()
print(sin.sin_amt+sin.gin)
#39
class com_lab_a:
    gin=56
class com_lab_b(com_lab_a):
    sid=20
s=com_lab_b()
print(s.gin)

#40 
------------------------
class a:
    def bike(self):
        print("hi")
class b:
    def car(self):
        print("helloo")
class c(a,b):
    def car(self):
        print("how r u")
obj=c()
obj.car()

#41
------------------
class a:
    def car(self):
        print("hi")
class b:
    def car(self):
        print("helloo")
class c(a,b):
    def bike(self):
        print("how r u")
obj=c()
obj.car()

#42 Multiple Inheritance: two or more parents and one child.
-----------------------------------------------------------------
class a:
    def __init__(self):
        print("hi")
class b:
    def __init__(self):
        print("helloo")
class c(b,a):
    def bike(self):
        print("how r u")
obj=c()
obj.bike()

#43
--------------
class a:
    def __init__(self):
        print("hi")
class b:
    def car(self):
        print("helloo")
class c(a,b):
    def __init__(self):
        super().__init__()
    def aero(self):
        print("how r u")
obj=c()
obj.aero()

#44 multi-level Inheritance:grand parent and parent and child.
----------------------------------------------------------------
class a:
    gin=30
class b(a):
    gin=10
class c(b):
    gin=40
obj=c()
print(obj.gin)

#45 
-------------------------------
class a:
    gin=30
class b(a):
    pass
class c(b):
    pass
obj=c()
print(obj.gin)

#46
-----------------------------------
class a:
    def __init__(self):
        print("a")
class b(a):
    def __init__(self):
        print("b")
class c(b):
    pass
obj=c()

#47
--------------------------------------
class a:
    def __init__(self):
        print("a")
class b(a):
    def __init__(self):
        print("b")
class c(b):
    pass
c()

#48
----------------------------
class a:
    def __init__(self):
        print("a")
class b(a):
    def __init__(self):
        print("b")
    def bike(self):
        print("bike")
class c(b):
    pass
c().bike()
c().bike()

#49 hierarchial Inheritance: One parent class and two child classes.
---------------------------------------------------------------------------
class a:
    def __init__(self):
        print("a")
class b(a):
    def bike(self):
        print("bike")
class c(b):
    pass
b()

#50 Hybrid Inheritance: combination of two or more inheritances.
-------------------------------------------------------------------------
class a:
    def __init__(self):
        print("a")
class b(a):
    def bike(self):
        print("bike")
class c(b):
    pass
class m(b):
    pass
b()

#51
----------------------------------------
class a:
    def __init__(self):
        print("a")
class b(a):
    def bike(self):
        print("bike")
class c(a):
    pass
class m(b,c):
    pass
m()

#52 Encapsulation
--------------------------------
class gin:
    _a=10
class sin(gin):
    def __init__(self):
        print(super()._a)
    pass
sin()

#53
------------------------------
class com_lab:
    def __init__(self):
        self.__locker()
    def __locker(self):
        print(1000000)
com_lab()

#54 method overriding
---------------------------------
class a:
    def sin(self,amt):
        print(amt)
class b(a):
    def sin(self,amt):
        print("1",amt)
a().sin(45)

#55 Duck typing:different class having same method name but without inheritance
-----------------------------------------------------------------------------------
class a:
    def sin(self,amt):
        print(amt)
class b:
    def sin(self,amt):
        print("1",amt)
b().sin(45)

#56 
---------------------
class dog:
    def sound(self):
        print("bow")
class cat:
    def sound(self):
        print("meow")
class duck:
    def sound(self):
        print("quack")
def makee_sound(obj):
    obj.sound()
d=dog()
c=cat()
du=duck()
makee_sound(du)

#57
-----------------------------
class cse:
    def __init__(self,t,e,m,s,so,h):
        self.t=t 
        self.e=e 
        self.m=m
        self.s=s
        self.so=so
        self.h=h
    def total(self):
        return (self.t+self.e+self.m+self.s+self.so+self.h)
    def avg(self):
        return (self.total()/6)
gin=cse(45,34,34,56,67,34)
sid=cse(34,65,46,67,23,74)
kin=cse(45,56,67,94,35,75)
print(kin.total())
print(kin.avg())

#58
-----------------------------------------
class cse:
    def __init__(self,name):
        print(f"Details of {name}")
        self.t= int(input("TELUGU : "))
        self.e=int(input("ENGLISH : "))
        self.m =int(input("MATHS : "))
        self.s = int(input("SCIENCE : "))
        self.so =int(input("SOCIAL : "))
    def total(self):
        return (self.t+ self.e+self.m+self.s+self.so)
    def avg(self):
        return self.total() / 5
narasimha = cse("NARASHIMA")
yuvaraj = cse("yuvaraj")
pavan  = cse("pavan")


PATTERNS:-----------------------
#=========== 1
#LEFT ANGLE TRIANGLE
# n=5
# *
# * *
# * * *
# * * * *
# * * * * *

n = 5
for i in range(1,n+1):
    print("* "*i)

#=========== 2
#DOWN LEFT ANGLE TRIANGLE
# n=5
# * * * * *
# * * * *
# * * *
# * *
# *
n = 5
for i in range(n,0,-1):
    print("* " * i)


# ================== 3

# *
# * *
# * * *
# * * * *
# * * * * *
# * * * *
# * * *
# * *
# *
n = 5
for i in range(1,n):
    print("* "*i)
for i in range(n,0,-1):
    print("* " * i)


#======================= 4

# ________*
# ______* *
# ____* * *
# __* * * *
# * * * * *
n=5
for i in range(1,n+1):
    print("  "*(n-i)+ "* "*i)

#======================= 5

# * * * * *
#   * * * *
#     * * *
#       * *
#         *
n = 5
for i in range(n,0,-1):
    print("  " * (n - i) + "* " * i)

#===================== 6
#         *
#       * *
#     * * *
#   * * * *
# * * * * *
#   * * * *
#     * * *
#       * *
#         *
n=5
for i in range(1,n):
    print("  "*(n-i)+ "* "*i)
for i in range(n,0,-1):
    print("  " * (n - i) + "* " * i)

#=====================  7
#     *
#    * *
#   * * *
#  * * * *
# * * * * *
n=100
for i in range(1,n+1):
    print(" "*(n-i)+ "* "*i)

#=================== 8
# * * * * *
#  * * * *
#   * * *
#    * *
#     *
n=5
for i in range(n,0,-1):
    print(" "*(n-i)+ "* "*i)


#================ 9
#   *
#  * *
# * * *
#  * *
#   *
n=3
for i in range(1,n):
    print(" "*(n-i)+ "* "*i)
for i in range(n,0,-1):
    print(" " * (n - i) + "* " * i)


#=================== 10
# * * * *
# *     *
# *     *
# * * * *
n =10
for i in range(1,n+1):
    if i == 1 or i == n: print("* "*n)
    else: print("* "+"  "*(n-2)+"* ")
#============  2 for
n = 9
for i in  range(1,n+1):
    for j in range(1,n+1):
        if i==1 or j == 1 or i == n or j == n:
            print("* ",end="")
        else: print("  ",end="")
    print()

#================== 11

# *     *
#   * *
#   * *
# *     *
#
# *       *
#   *   *
#     *
#   *   *
# *       *

n = 55
for i in range(1,n+1):
    for j in range(1,n+1):
        if  i==j or (i+j)==(n+1):
            print("* ",end="")
        else:
            print("  ",end="")
    print()


# ==============  12
# * * * * *
# * *   * *
# *   *   *
# * *   * *
# * * * * *
n = 55
for i in range(1,n+1):
    for j in range(1,n+1):
        if i==1 or j == 1 or i == n or j == n or i==j or (i+j)==(n+1):
            print("* ",end="")
        else:
            print("  ",end="")
    print()
# ==============  13

# 1
# 1 2
# 1 2 3
n = 10
for i in range(1,n+1):
    for j in range(1,i+1):
        print(j,end=" ")
    print()

# ==============  14

# 1
# 2 2
# 3 3 3
# 4 4 4 4
n = 10
for i in range(1,n+1):
    for j in range(1,i+1):
        print(i,end=" ")
    print()

# ==============  15
# 1
# 2 3
# 4 5 6
# 7 8 9 10
n = 10
k=1
for i in range(1,n+1):
    for j in range(1,i+1):
        print(k,end=" ")
        k+=1
    print()

# ==============  16
# n = 1<= n >=26
# a
# a b
# a b c
# a b c d
n=5
for i in range(1,n+1):
    for j in range(0,i):
        print( chr(ord("a") +j ),end=" ")
    print()
# ==============  17
# a
# b b
# c c c
n=26
for i in range(0,n):
    for j in range(0,i+1):
        print( chr(ord("a") +i),end=" ")
    print()

# ==============  18

# s = raju
# r
# ra
# raj
# raju
# raj
# ra
# r
s="ram"
for i in range(1,len(s)):
    print(s[:i])
for i in range(len(s),0,-1):
        print(s[:i])




