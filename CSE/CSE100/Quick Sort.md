A sorting algorithm with worst-case time complexity $O(n^2)$ which makes up for it by having expected running time $O(nlogn)$ with small constant scalars and sorting in-place.

It works similarly to [[Merge Sort]]: Partition the array into two subarrays such that every item in the first subarray is lesser than the item at the point of partition, and every item in the second subarray is greater than the item at the point of partition.
The point of partition(and the item at that point) is called the Pivot. Choosing a good Pivot is a task in and of itself, which has not been covered in lecture yet. More discussion of Pivots during the running time analysis of the [[K-Select]] problem.

[[Asymptotic Analysis]] comparing different implementations of Quick Sort and [[Merge Sort]] finds that the two algorithms are extremely comparable, but in practice Quick Sort can often be preferable, as they are $O()$ the same time complexity but Quick Sort will typically contain smaller constant scalars.

The ideal pivot for Quick Sort is the median of the dataset. In this case, the running time is $T(n)=O(nlog(n))$.
Despite sorting in-place, this uses a [[Divide and Conquer]] framework.

The most common version of this is a [[Randomized Algorithm]], which picks a random point at which to partition the array. This is because in a non-sorted list, you cannot reliably pick the median, so we leave it up to chance. In the [[K-Select]] problem we set up a framework for approximating the median, and this also is pretty cool.

Below is the randomized version, if you want to manually pick a pivot(or change the method by which pivots are picked) you can do that by bypassing `RandomPartition` and going straight to `Partition`.

Before the code, a prolonged discussion of the [[Randomized Algorithm]] version of this;
the expected number of comparisons is $$E[\Sigma_{a=1}^{n-1}\Sigma_{b=a+1}^nX_{a,b}]$$
Which can have its expectation distributed to be:$$\Sigma_{a=1}^{n-1}\Sigma_{b=a+1}^nE[X_{a,b}]$$
And that $E[X_{a,b}]$ can be solved for $2/(b-a+1)$(See lecture slides for 10/22-2024 for that derivation), giving $$\Sigma_{a=1}^{n-1}\Sigma_{b=a+1}^n(2/(b-a+1))$$
and finally this is solvable for:$$2(n(H_{n-1})-(n-1)<=2n(ln(n))$$
With the harmonic number $H_{n-1}=\Theta(ln(n))$. That bit about the harmonic number is outside of the scope of the lecture, but I'm assured that it's contained within the textbook somewhere.

That silly little value of $2n(ln(n))$ is $O(nlog(n))$, so the expected number of comparisons for Quick Sort is $O(nlog(n))$, which in this case is also the value of the Expected Running Time. This can be proven by finding that for Quick Sort the running time is dominated by the number of comparisons.
With the randomness, an absolutely terrible pivot can still result in $O(n^2)$, but the odds of that are low enough that we don't typically worry about it.

This Pseudocode doesn't represent the in-place implementation found in the `c++` version below. I'll do something about that eventually, I think.
Pseudocode: 
```
Partition(A,p):
	L = new array
	R = new array
	for i=1,...,n:
		if i==p:
			continue
		else if A[i] <=A[p]:
			L.append(A[i])
		else if A[i]>A[p]:
			R.append(A[i])
	return L,A[p],R
```

`c++` implementation:
```
#include<iostream>

#include<cstdlib>

using namespace std;

  

int Partition(int* arr,int p,int r){

    int x=arr[r];

    int i=p-1;

    for(int j=p;j<=r-1;j++){

        if(arr[j]<x){

            i++;

            int placeholder=arr[i];

            arr[i]=arr[j];

            arr[j]=placeholder;

        }

    }

    int placeholder = arr[i+1];

    arr[i+1] = arr[r];

    arr[r]=placeholder;

    return(i+1);

}

  

int RandomPartition(int* arr,int p, int r){

    int range = (r-p+1);

    int i=rand() % range;

    i+=p;

    int placeholder=arr[r];

    arr[r]=arr[i];

    arr[i]=placeholder;

    return Partition(arr,p,r);

}

  

void RandomQuickSort(int* arr,int p, int r){

    if(p<r){

        int q=RandomPartition(arr,p,r);

        RandomQuickSort(arr,p,q-1);

        RandomQuickSort(arr,q+1,r);

    }

}

  

int main(){

    int length;

    cin>>length;

    int* arr = new int[length];

    for(int i=0;i<length;i++){

        cin>>arr[i];

    }

    RandomQuickSort(arr,0,length-1);

    for(int i=0;i<length;i++){

        cout<<arr[i]<<";";

    }

    return 1;

}
```