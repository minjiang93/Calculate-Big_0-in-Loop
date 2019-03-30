# Calculate-Big_0-in-Loop
The idea to calculate Big_0 in program loop

 1.//c is constant 
   for(int 1=0; i<c, i++){
    //some code over there. 
	  //but it is O(1)
     }
  //in this case, Big_O is O(1), because A loop or recursion that runs a constant number of times is also considered as O(1). 
 
2.  // n is unknown varliable
 for(int 1=0; i<n, i++){
    //some code over there. 
	//but it is O(1)
  }
 // In this program, the Big_O is O(N)

3.//n is unknown varliable
for (int i = 1; i <= n; i += c) {  
   // Here c is a constant   
   for (int i = 1; i <= c; i++) {  
      // some O(1) expressions
   }
}
for (int i = n; i > 0; i -= c) {
   // Here c is a constant   
   for (int i = 1; i <= c; i++) {  
      // some O(1) expressions
   }
}
//Time complexity = 2 * n * O(1) = 2 * O(1 * n) = O(n) ; In some case, it doesn't have two or more n, maybe many different unknown vaules, the Big_O always choose the worest case. It can be write as O(max(n,m,x..)

4.//nestcall n is unknown
for (i = 0; i < N; i++) {
    for (j = i+1; j < N; j++) {
        // some O(1) expressions
    }
}
//O(n)*O(n) = O(n^2)

5.//nestcall n,m is unknown
for (i = 0; i < N; i++) {
   for (j = 0; j < M; j++) {
      // some O(1) expressions
   }
}
//O(n)*O(m) = O(nm)

6.//binary search tree iterative 
for (int i = 1; i <= N; i *= c) {
   // some O(1) expressions
}
for (int i = N; i > 0; i /= c) {
   // some O(1) expressions
}
//Time Complexity of a loop is considered as O(log n) if the loop variables is divided / multiplied by a constant amount. 

7.// c is a constant greater than 1   
for (int i = 2; i <=n; i = pow(i, c)) { 
   // some O(1) expressions
}

// Here fun is sqrt or cuberoot or any other constant root
for (int i = n; i > 0; i = fun(i)) { 
   // some O(1) expressions
}
//Time Complexity of a loop is considered as O(loglog N) if the loop variables is reduced / increased exponentially by a constant amount.

8.//when loop is infeclted by i
f(N)
{
  int s, i;
  for (i=1, s=1; s<=n; i++, s+=i)
     printf("hello"); 
}
//If k is total number of iterations taken by the program, then the for loop terminates if: 1 + 2 + 3 ….+ k = [k(k+1)/2] > n
==> So k = O(√n). 
