# Data Structures and Algorithms
  repo  นี้ สร้างไว้เพื่อทบทวนบนเรียนของ วิชา Data Structures and Algorithms มันอาจจะดูงงเพราะผม ก็จะพยามเข้าใจมัน 
## เนื้อหาที่มีสอนในห้อง 
   #### Algorithms 
   -    การวเิคราะห์ algorithm 
   -    Algorithm ในการเรียงลำดับข้อมูล 
   -    Algorithm ในการค้นหาข้อมลู 
   #### Data Structures 
   -    โครงสรา้งขอ้มลู array, link list 
   -    โครงสรา้งขอ้มลู queue, stack, graph and tree Binary tree, B tree and Heap 
   #### กลยทุธข์อง algorithm 
   
## Data Structures คืออะไร 
   Data Structures คือประเภทข้อมูลที่มีการจัดเรียง เเล้วมีความความสัมพันธ์เเบบต่างๆ มีกฎข้อบังคับอย่างมีระบบ ข้อมูลอาจเป็นชนิดเดียวกันหรือต่างกันก็ได้  เช่น  array ,string 
    ในโปรเเกรมคอมพิวเตอร์โปรเเกรมหนึ่ง เราสามรถมองเเเยกออกได้ 2 ส่วน คือ Data Structures เเละ Algorithms  
####  Data Structures ที่ดี
   -   Decomposed –– สามารถแยกเป็นส่วนหรือหน่วยย่อยได้
   -   Access –– มีวิธีการในการเข้าถึงหน่วยข้อมูล 
   -   Store –– มวีธิการในการจัดเก็บหน่วยข้อมูล
   -   Encapsulated ––  ควรปกปิดกระบวนการที่ซับซ้อนในการสร้าง หรือเข้าถึงหน่วยข้อมูล 
   -   Real world relation ––  สามารถสะท้อนความสัมพันธ์ข้อมูลกับ โลกของความเป็นจริงได้
   -   Easy to Design & Easy to Implement –– ง่ายในการออกแบบ และเขียนโปรแกรม
#### ประเภทของ Data Strctures 
   -  Linear Data Structure
      -   Array Link List Stack Queue 
   -  Linear Data Structure
      -   Tree Graph
## Algorithms คืออะไร  
  กระบวนการ/ข้อตอน ในการเเก้ไขปัญหาให้ ให้บรรลุเป้าหมาย 
      - การทำงานมึจุดจบ เรียบง่ายคอมสามารถทำงานได้ ไม่กำกวม
  การอธิบาย Algorithms นั้นจะมีการนำเสนอเเบบ flow chart pseudo code หรือ เขียนอธิบายขั้นตอน
## การวิเคราะห์ Algorithms
   ปัญหาหนึ่งปํญหาสามารถเเก้ด้วย Algorithms หลายเเบบได้ ดังนั้นจึงมึการวิเคราะห์ Algorithms เพื่อจะตรวจสอบว่า  Algorithms ไหนใช้เเก้ปัญหาได้มีประสิทธิภาพมากกว่า 
  - การวิเคราะห์ Algorithms ที่เรียนใช้ class 
    - วเิคราะหด์ว้ย Time Complexity
      - หา units of time ด้วยการนับจำนวนคำสั่ง (instruction count) 
      - หา units of time ด้วยการนับจำนวนตวัดำเนินการ (operation count) 
      - การหาฟังก์ชันการเติบโต (growth of function) ของ algorithm: T(n) จาก units of time 
      - การหา Big O 
## การวิเคราะห์ Algorithms  --  วิเคราะหอ์ย่างไร 
   การวิเคราะห์ประสิทธิภาพการของ Algorithms  สามารถทำได้หลายเเบบ เช่น 
  - เวลาที่ใช้ในการประมวลผลข้อมูล
    - Time complexity 
  - พื้นที่ในการจัดเก็บข้อมลู 
    - Space complexity 
  * Time and  Space ยิ่งน้อยยิ่งดี 
####  การวิเคราะห์ ด้วยเวลา(Time) เเละ เเละการใช้พื้นที่(Space)น้อยนั้น ทำได้ยาก !! ###

### ดังนั้นจะกลาวถึงเฉพาะ  Time Complexity
   - units of time ทั้งเเบบ instruction count and operation count 
##  Time Complexity
   uinit of time  จะนำไปสู่ Function การเติบโต T(n) เเล้วจะนำไปสู่ Big O 
   การนับ uinit of time  ทำได้สอบเเบบคือ instruction เเละ operation
## การนับ uinit of time เเบบ  instruction
   การนับเเบบ instruction จะนับจะเพราะส่วนที่เป็น คำส่ง 
```
  int num;  // ไม่นับ 
  num = 0;  // 1  
```
### Ex1 
  ```
  int num,sum;      // ไม่นับ
  num=sum=0;        // 1 
  for(i=0;i<=n;i++) // 1+(n+2)+n+1 =  2n+3
  {                 // ไม่นับ
        num++;      // 2 คำสัง ทำ n Loop
        sum+=num;   // = 2n+2
  }                 // ไม่นับ
  ```
  * T(n)
  ```
  T(n) 2n+3+2n+2 = 4n+5 = O(T(n))=O(n)
  ```
### Ex2 
```
int num =0;         // 1 
int i =0;           // 1
while(i<n){         // n+1
    i+=i+1;         // สองคำสั่งทำ n+1 รอบ 2n+2
    num+=i*2;       //
}
```
* T(n)
```
T(n) 1+1+n+1+2n+2 = 3n+5 O(T(n)) = O(n)
```
### Ex3 
```
int num,i,j;        // ไม่นับ
num=0;              // 1
for(i=0;i<=n;i++){  // 1+n+1+n  = 2n+2
  for(j=0;j<n;j++){   n*[2n+2] = 2n^2+2n
     num+=i;        // 2 คำสั่ง ทำ n^2 รอบ = 2n^2
     num++;         // 
  }
}
```
* T(n)
```
T(n) 1+2n+2+2n^2+2n+2n^2=4n^2+4n+3 = O(T(n))=O(n^2)
```
## การนับ uinit of time เเบบ  operation
   การนับเเบบ Operation จะนับจะเพราะส่วนที่เป็น operation +-*/ []
```
  int num,num1[];   // ไม่นับ 
  num = 0;          // 1  
  num=num1[0];      // 2 ; = and [] 
```
### Ex1 
```
int num,sum;        // ไม่นับ
  num=sum=0;        // 1 
  for(i=0;i<=n;i++) // 1+(n+2)+n+1 =  2n+3
  {                 // ไม่นับ
        num++;      // 1 opreration ทำ n+1 รอบ n+1 รอบ
        sum+=num;   // 2 opreration ทำ n+1 รอบ 2n+2
  }                 // ไม่นับ
```
* T(n)
```
 1+2n+3+n+1+2n+2=5n+7 = O(T(n))=O(n)
```
### Ex2 
```
int num,i,j;        // ไม่นับ
num=0;              // 1
for(i=0;i<=n;i++){  // 1+n+1+n  = 2n+2
  for(j=0;j<n;j++){   n*[2n+2] = 2n^2+2n
     num+=i;        // 2 opreration ทำ n^2 รอบ = 2n^2
     num++;         // 1 opreration ทำ  n^2 รอบ
  }
}
```
* T(n)
```
T(n) 1+2n+2+2n^2+2n+2n^2+2n^2=5n^2+4n+3 = O(T(n))=O(n^2)
```
## Sorting 
* Selection Sort  
* Insertion Sort 
* Bubble Sort 
* Merge Sort 
* Quick Sort 
* Heap Sort 
* Radix Sort
