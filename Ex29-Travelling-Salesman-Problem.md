# Ex 6d Travelling Salesman Problem
## DATE:12/5/25
## AIM:
To write a C Program to implement Travelling Salesman Problem for finding shortest path.
## Algorithm
1.Start

2.Read the number of cities n and the adjacency matrix a representing the distances between cities.

3.Initialize a visited array to track which cities have been visited.

4.Start the process with city 0 and print its number.

5.In the mincost function, find the nearest unvisited city using the least function.

6.If all cities are visited, return to the starting city (city 0) and finish.

7.In the least function, find the unvisited city with the smallest cost from the current city, and update the cost.

8.Print the minimum cost of the route after visiting all cities.

9.End 

## Program:

```
Program to implement Travelling Salesman Problem for finding shortest path
Developed by: Varshini D
RegisterNumber:  212223230234

#include<stdio.h>
int a[10][10],visited[10],n,cost=0;

voidget()
{
int i,j;
scanf("%d",&n);
for(i=0;i< n;i++)
{
for( j=0;j < n;j++) scanf("%d",&a[i][j]);
visited[i]=0;
}
}
voidmincost(int city)
{
int ncity;
int least(int); visited[city]=1; printf("%d-->",city+1); ncity=least(city);

if(ncity==999)
{
ncity=0; printf("%d",ncity+1); cost+=a[city][ncity]; return;
}
mincost(ncity);
}
int least(intc)
{
int i,nc=999;
int min=999,kmin; for(i=0;i < n;i++)
{
if((a[c][i]!=0)&&(visited[i]==0)) if(a[c][i] < min)
{

if(a[c][i] < min)
{
min=a[i][0]+a[c][i];
kmin=a[c][i];
nc=i;
}
if(min!=999)
cost+=kmin; returnnc;

min=a[i][0]+a[c][i]; kmin=a[c][i]; nc=i;
voidput()
{
printf("\n\nMinimum cost:%d",cost);
}
int main()
{
get(); mincost(0); put(); return 0;
}
```


## Output:

<img width="383" alt="image" src="https://github.com/user-attachments/assets/55f5ebd0-e351-4698-8511-8a7ab163cd5a" />


## Result:
Thus, the C program to implement Travelling Salesman Problem for finding shortest path is implemented successfully.
