# Data-structure-and-Algorithm

//----------------------------C++数据结构与算法：01——Fibonacci-------------------------------------
#include "stdafx.h"
#include<iostream>
using namespace std; 

//fib1：二分递归计算Fibonacci数列的第n项：O(2^n)，复杂度高，效率低
int fib1( int n )  //二分递归计算Fibonacci数列的第n项：O(2^n)
{ 
    return ( 2 > n ) ?
           n //若到达递归基，直接取值
           : ( fib1 ( n - 1 ) + fib1 ( n - 2 ) )  % ( 1 << 30 ); //否则，递归计算前两项，其和即为正解
}

int main ( ) 
{
    int n;
    scanf( "%d", &n );
    printf( "%d\n", fib1( n ) );
	  system("pause"); //阻止控制台应用闪退问题，注意：要在return语句之前
    return 0;
}
