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
## นิยามของ Big O
```
ให้ T(n) เเละ f(n) เป็นฟังก์ชั่นใดๆ
T(n)=O(f(n)) ถ้ามีค่าคงที่ที่เป็นค่าบวก c เเละ n0(n ศูนย์)  ที่ทำให้
T(n)<=c*f(n) เมือ n>=n0;
```
### Ex1 
  T(n)=2n-4 ,f(n)=n
  ต้องการหาว่า T(n)=O(f(n)) หรือไม
  กำหนดให้ c=3 ,n0=1
  2(1)-4<=3*(1) 
  -2<=3 เป็นจริง
  ดังนั้น ``` T(n)=O(n) ```
## Sorting 
  Sorting เป็น  Algorithms ที่ใช้ในการเรียงข้อมูล มีหลายเเบบดังนี้
* Selection Sort  
* Insertion Sort 
* Bubble Sort 
* Merge Sort 
* Quick Sort 
* Heap Sort 
* Radix Sort

###  Selection Sort 
   Selection Sort เป็น Algorithm ในการเรียงข้อมูลเเบบหนึ่ง หลังการทำงาน จะค้นหาข้อมูลที่น้อยหรือมากที่สุดเเล้วนำมาเรียงไว้ทางด้ายช้ายมือของชุดช้อมูล 
  ```c
   void SeletionSort(int a[],int len){
	    int pass,i,ind,temp;
	for(pass=0;pass<len;pass++){
		   ind=pass;
	 for(i=pass+1;i<len;i++){
		if(a[i]<a[ind]){
			 swap(&a[i],&a[ind]);
		    }
		  }
	  }
  }
  ```
###  Insertion Sort 
   Insertion Sort จะมีหลังการทำงานคือ เปรียบเทียบข้อมูลระหว่างคู่ เเล้วถ้าข้อมูลน้อยกว่าให้สลับข้อมูลมาไว้ทางซ้ายมือ 
  ```c
    void InserttionSort(int a[],int len){
	    int i,j,key;
	    for(i=1;i<len;i++){
		    key =a[i];
		    j=i-1;
		    while(j>=0&&a[j]>key){
			      a[j+1]=a[j];
			      j--;
		    }
		      a[j+1]=key;
	    }
  }
  ```
###  Bubble Sort
   Bubble Sort  มีหลังการทำงาน คือ เปรียบเทียบข้อมูลจากทางขาวมือถ้าข้อมูลขาวมือมากกว่าด้านซ้ายมือจะสลับต่ำเเหน่งข้อมูลเเต่ถ้าขาวมือมากกว่าจะเอาไว้ทีเดิมเเล้วเทียบข้อมูลถัดไป 
   ```c 
   void bubleSort(int a[],int len){
	    int i,pass,temp,swapped; 
	    for(pass=1;pass<len;pass++){
		    swapped=0;
		    for(i=0;i<len-pass;i++){
		      if(a[i]>a[i+1]){
			      swap(&a[i],&a[i+1]);
			      swapped=1;
		      }
	    }
	      if(!swapped)
	 	      return;
//	 printArray(a,len);
      }
    }
   ```   
###  Merge Sort 
   Merge Sort จะเเยกข้อมูลออกเป็นกลุ่มเล็กที่สุดเเล้วค่อย รวมจากกลุ่มเล็กสุดโดยมีการเรียงในกลุ่มนั้น เเล้วรวมเป็นกลุ่มใหญ่เรื่อยๆ 
###  Quick Sort
   เลือก pivot ของข้อมูลเพื่อจะเอามาใช้ในการเรียงข้อมูล pivot จะเป็นค่าที่สำคัญถ้าเลือก piovt ดีจะสามารถเเบ่งครึ่งข้อมูลได้ หลังการทำงานคือ ให้เลือก pivot เเล้วเอา pivot ไปสลับกับข้อมูล left เเล้วระบุตำเเหน่ง ให้ต่ำเเหน่ง lo เป็น left+1 เเล้ว hi เป็นต่ำเเหน่ง right (ค่าสุดท้ายข้อมูล)
   เเล้ว check lo ว่าต่ำเเหนงที่อยู่ มันมีค่าของข้อมูล มากกว่า pivot ไหม ถ้ามีให้ หยุดเเต่ถ้าไม่มีให้เลือนไปต่ำเเหน่งถัดไป เเล้วไปดู hi เเต่ hi ต้องหาค่าที่ น้อยกว่า pivot เเล้วถ้าเจอก็หยุด เมื่อเราได้ต่ำเเหน่งเเล้วเราก็ทำการสลับต่ำเเหน่งข้อมูล เเล้วถ้าต่ำเเหน่ง hi กับ lo เลือมกัน ก็ให้สลับต่ำเเหน่ง  
   pivot กับ hi เเล้วก็ใช้ pivot เเบบข้อมูลออกเป็นสองกลุ่ม เเล้วก็ทำเหมือนเดิม 
###  Heap Sort
    ทำให้เป็น complte binary 
###  Radix Sort
    เรียงจากตัวท้ายสุดเเล้วจัดกลุ่ม
### Liner Search 
  การทำงานจะไลหาจากข้อมูลทั้งมูล หมด
  ```c
  int lSearch(int a[],int len,int key){
	int i;
	for(i=0;i<len;i++){
		if(a[i]==key)
			return i;
	   }
	return -1;
  }
  ```
### Binary Search 
  จะทำการเรียงข้อมูลก่อนการค้นหา  มากไปน้อย หรือ น้อยไปมากก็ได้
  ```c
  int bSearch(int a[],int len,int key){
	int left,right,mid;
	left=0;
	right=len-1;
	mid=(left+right)/2;
	while(left<=right){
		if(a[mid]==key)
			return mid;
		else if(a[mid]<key)
			left=mid+1;
		else 
			right=mid-1;
		mid=(left+right)/2;
	  }
	return -1;
  }
  ```