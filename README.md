
// 1. Print numbers from 1 to 10, but skip 5 using continue
// ============================================================
#include<iostream>
using namespace std;
int main(){
 for(int i=1;i<=10;i++){
  if(i==5) continue;
  cout<<i<<"\n";
 }
 return 0;
}

/*
Output:
1
2
3
4
6
7
8
9
10
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 2. Print numbers from 1 to 10, but stop at 7 using break
// ============================================================
#include<iostream>
using namespace std;
int main(){
 for(int i=1;i<=10;i++){
  if(i==7) break;
  cout<<i<<"\n";
 }
 return 0;
}

/*
Output:
1
2
3
4
5
6
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 3. Search for a Number in a Sequence; Stop if Found (break)
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,x,found=0;
 cout<<"Enter size: "; cin>>n;
 int a[n];
 cout<<"Enter elements: ";
 for(int i=0;i<n;i++) cin>>a[i];
 cout<<"Search: "; cin>>x;
 for(int i=0;i<n;i++){
  if(a[i]==x){ found=1; break; }
 }
 cout<<(found?"Found":"Not Found");
 return 0;
}

/*
Output:
Enter size: 5
Enter elements: 2 4 6 8 10
Search: 6
Found
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 4. Display Even Numbers 1–20, Skip Multiples of 4 (continue)
// ============================================================
#include<iostream>
using namespace std;
int main(){
 for(int i=1;i<=20;i++){
  if(i%2!=0) continue;
  if(i%4==0) continue;
  cout<<i<<"\n";
 }
 return 0;
}

/*
Output:
2
6
10
14
18
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 5. Menu-driven Calculator using switch (with default)
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int a,b; char op;
 cout<<"Enter a b: "; cin>>a>>b;
 cout<<"Enter operator(+,-,*,/): "; cin>>op;
 switch(op){
  case '+': cout<<"Sum="<<a+b; break;
  case '-': cout<<"Diff="<<a-b; break;
  case '*': cout<<"Prod="<<a*b; break;
  case '/': cout<<"Div="<<a/b; break;
  default: cout<<"Invalid operator!";
 }
 return 0;
}

/*
Output:
Enter a b: 4 2
Enter operator(+,-,*,/): *
Prod=8
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 6. Check if Number is Prime (terminate early using break)
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,flag=0;
 cout<<"Enter number: "; cin>>n;
 for(int i=2;i<n;i++){
  if(n%i==0){ flag=1; break; }
 }
 cout<<(flag?"Not Prime":"Prime");
 return 0;
}

/*
Output:
Enter number: 7
Prime
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 7. Read Numbers until -1, Skip Negatives using continue
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n;
 cout<<"Enter numbers (-1 to stop):\n";
 while(true){
  cin>>n;
  if(n==-1) break;
  if(n<0) continue;
  cout<<n<<" ";
 }
 return 0;
}

/*
Output:
Enter numbers (-1 to stop):
5 2 -3 7 -1
5 2 7
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 8. Multiplication Table, Stop When Product > 50
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n;
 cout<<"Enter number: "; cin>>n;
 for(int i=1;i<=10;i++){
  if(n*i>50) break;
  cout<<n<<" x "<<i<<" = "<<n*i<<"\n";
 }
 return 0;
}

/*
Output:
Enter number: 7
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
7 x 6 = 42
7 x 7 = 49
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 9. Demonstrate default case in switch
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int ch=3;
 switch(ch){
  case 1: cout<<"Case 1"; break;
  case 2: cout<<"Case 2"; break;
  default: cout<<"Default Case";
 }
 return 0;
}

/*
Output:
Default Case
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 10. Count Positive Numbers until 0 (break)
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,c=0;
 cout<<"Enter numbers (0 to stop): ";
 while(true){
  cin>>n;
  if(n==0) break;
  if(n>0) c++;
 }
 cout<<"Positive count="<<c;
 return 0;
}

/*
Output:
Enter numbers (0 to stop): 3 5 -2 4 0
Positive count=3
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 11. Calculate Factorial using while loop
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,f=1,i=1;
 cout<<"Enter n: "; cin>>n;
 while(i<=n){ f*=i; i++; }
 cout<<"Factorial="<<f;
 return 0;
}

/*
Output:
Enter n: 5
Factorial=120
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 12. Generate Fibonacci Series using while loop
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,a=0,b=1,c=0,i=1;
 cout<<"Enter terms: "; cin>>n;
 while(i<=n){
  cout<<a<<" ";
  c=a+b; a=b; b=c;
  i++;
 }
 return 0;
}

/*
Output:
Enter terms: 7
0 1 1 2 3 5 8
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 13. Find and Print All Prime Numbers between 1 and N
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n;
 cout<<"Enter N: "; cin>>n;
 for(int i=2;i<=n;i++){
  int f=0;
  for(int j=2;j<i;j++){
   if(i%j==0){ f=1; break; }
  }
  if(f==0) cout<<i<<" ";
 }
 return 0;
}

/*
Output:
Enter N: 20
2 3 5 7 11 13 17 19
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 14. Check Whether a Given Number is Armstrong or Not
// ============================================================
#include<iostream>
#include<cmath>
using namespace std;
int main(){
 int n,rem,sum=0,temp;
 cout<<"Enter number: "; cin>>n;
 temp=n;
 while(n>0){ rem=n%10; sum+=pow(rem,3); n/=10; }
 cout<<(sum==temp?"Armstrong":"Not Armstrong");
 return 0;
}

/*
Output:
Enter number: 153
Armstrong
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 15. Display Armstrong Numbers between 1 and 500
// ============================================================
#include<iostream>
#include<cmath>
using namespace std;
int main(){
 int n,rem,sum;
 for(int i=1;i<=500;i++){
  n=i; sum=0;
  while(n>0){ rem=n%10; sum+=pow(rem,3); n/=10; }
  if(sum==i) cout<<i<<" ";
 }
 return 0;
}

/*
Output:
1 153 370 371 407
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 16. Check Whether a Number is Perfect Number
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,sum=0;
 cout<<"Enter number: "; cin>>n;
 for(int i=1;i<n;i++) if(n%i==0) sum+=i;
 cout<<(sum==n?"Perfect":"Not Perfect");
 return 0;
}

/*
Output:
Enter number: 28
Perfect
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 17. Display All Perfect Numbers between 1 and 1000
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int sum;
 for(int n=1;n<=1000;n++){
  sum=0;
  for(int i=1;i<n;i++) if(n%i==0) sum+=i;
  if(sum==n) cout<<n<<" ";
 }
 return 0;
}

/*
Output:
6 28 496
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 18. Check Whether a Number is Strong Number
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,temp,rem,sum=0,f;
 cout<<"Enter number: "; cin>>n;
 temp=n;
 while(n>0){
  rem=n%10; f=1;
  for(int i=1;i<=rem;i++) f*=i;
  sum+=f; n/=10;
 }
 cout<<(sum==temp?"Strong":"Not Strong");
 return 0;
}

/*
Output:
Enter number: 145
Strong
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 19. Display All Strong Numbers between 1 and 500
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,rem,sum,f;
 for(int i=1;i<=500;i++){
  n=i; sum=0;
  while(n>0){
   rem=n%10; f=1;
   for(int j=1;j<=rem;j++) f*=j;
   sum+=f; n/=10;
  }
  if(sum==i) cout<<i<<" ";
 }
 return 0;
}

/*
Output:
1 2 145
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 20. Reverse a Number and Check if Palindrome
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,rev=0,temp;
 cout<<"Enter number: "; cin>>n;
 temp=n;
 while(n>0){ rev=rev*10+n%10; n/=10; }
 cout<<"Reverse="<<rev<<"\n";
 cout<<(rev==temp?"Palindrome":"Not Palindrome");
 return 0;
}

/*
Output:
Enter number: 121
Reverse=121
Palindrome
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 21. Find Sum of All Even and Odd Digits in a Number
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,rem,es=0,os=0;
 cout<<"Enter number: "; cin>>n;
 while(n>0){
  rem=n%10;
  if(rem%2==0) es+=rem; else os+=rem;
  n/=10;
 }
 cout<<"EvenSum="<<es<<"\nOddSum="<<os;
 return 0;
}

/*
Output:
Enter number: 123456
EvenSum=12
OddSum=9
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 22. Check Whether a Number is Harshad Number
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,sum=0,temp;
 cout<<"Enter number: "; cin>>n;
 temp=n;
 while(n>0){ sum+=n%10; n/=10; }
 cout<<(temp%sum==0?"Harshad":"Not Harshad");
 return 0;
}

/*
Output:
Enter number: 18
Harshad
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 23. Display All Harshad Numbers between 1 and 100
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,sum,temp;
 for(int i=1;i<=100;i++){
  n=i; sum=0;
  while(n>0){ sum+=n%10; n/=10; }
  if(i%sum==0) cout<<i<<" ";
 }
 return 0;
}

/*
Output:
1 2 3 4 5 6 7 8 9 10 12 18 20 21 ...
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 24. Display Multiplication Tables from 1 to 10
// ============================================================
#include<iostream>
using namespace std;
int main(){
 for(int i=1;i<=10;i++){
  for(int j=1;j<=10;j++) cout<<i*j<<"\t";
  cout<<"\n";
 }
 return 0;
}

/*
Output (partial):
1 2 3 4 5 6 7 8 9 10
2 4 6 8 10 12 14 16 18 20
...
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 25. Print Prime Factors of a Given Number
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n;
 cout<<"Enter number: "; cin>>n;
 cout<<"Prime factors: ";
 for(int i=2;i<=n;i++){
  while(n%i==0){ cout<<i<<" "; n/=i; }
 }
 return 0;
}

/*
Output:
Enter number: 84
Prime factors: 2 2 3 7
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 26. Find LCM of Two Numbers using Loops
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int a,b,max;
 cout<<"Enter a b: "; cin>>a>>b;
 max=(a>b)?a:b;
 while(true){
  if(max%a==0 && max%b==0){ cout<<"LCM="<<max; break; }
  max++;
 }
 return 0;
}

/*
Output:
Enter a b: 4 6
LCM=12
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 27. Find GCD of Two Numbers using Loops
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int a,b,gcd;
 cout<<"Enter a b: "; cin>>a>>b;
 for(int i=1;i<=a&&i<=b;i++)
  if(a%i==0 && b%i==0) gcd=i;
 cout<<"GCD="<<gcd;
 return 0;
}

/*
Output:
Enter a b: 8 12
GCD=4
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 28. Display Sum of Series: 1 + 2 + 3 + ... + N
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,sum=0;
 cout<<"Enter N: "; cin>>n;
 for(int i=1;i<=n;i++) sum+=i;
 cout<<"Sum="<<sum;
 return 0;
}

/*
Output:
Enter N: 5
Sum=15
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 29. Display Sum of Series: 1² + 2² + 3² + ... + N²
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,sum=0;
 cout<<"Enter N: "; cin>>n;
 for(int i=1;i<=n;i++) sum+=i*i;
 cout<<"Sum="<<sum;
 return 0;
}

/*
Output:
Enter N: 5
Sum=55
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 30. Display Sum of Series: 1³ + 2³ + 3³ + ... + N³
// ============================================================
#include<iostream>
using namespace std;
int main(){
 int n,sum=0;
 cout<<"Enter N: "; cin>>n;
 for(int i=1;i<=n;i++) sum+=i*i*i;
 cout<<"Sum="<<sum;
 return 0;
}

/*
Output:
Enter N: 5
Sum=225
*/

cout<<"\n--------------------------------------------\n";
