
A more complicated but also more efficient sorting algorithm from [[Insertion Sort]], using a [[Divide and Conquer]] principle.

Split the array in half recursively until you have n arrays of length 1(and all 1-item-long arrays are intrinsically sorted), then merge the two halves in a sorted fashion.

The merging is the hard part, combining those 1-length lists back together:
Do this by putting the items from the component lists into the merged list in least-to-greatest fashion, as shown below:
Because the two component lists you are merging are guaranteed to be sorted, the smallest item which you have not yet put into the merged list is guaranteed to be one of two items: The smallest item you have not yet sorted from the first list, or the smallest item you have not yet sorted from the second list. So, just continually look at those, adjusting indexes whenever you sort an item, and you can merge the two sorted lists.

Pseudocode:
```
MergeSort(A):
	n=length(A)
	if(n<=1):
		return A
	L = MergeSort(A[1:n/2])
	R = MergeSort(A[(n/2)+1:n])
	return Merge(L,R)

Merge
```
Pseudocode for the Merge section still pending, mostly because I'm too lazy to write it myself and it has yet to be presented.

Merge Sort's Time-Complexity is a recurrence relation, but luckily for me that relation's solution is known to be $O(nlog(n))$. This is a significant improvement over [[Insertion Sort]].
However, Merge Sort will still go through its entire process even if you give it an array that's already sorted.

c++ Implementation:
```
#include <iostream>

using namespace std;

int* MergeSort(int* arr, int n);

int* Merge(int* L, int* R, int n);

int main(){

    int length;

    cin>>length;

    int* values = new int[length];

    for(int i=0;i<length;i++){

        cin>>values[i];

    }

    int* result = MergeSort(values,length);

    for (int i=0;i<length;i++){

        cout<<result[i]<<";";

    }

    return 1;

}

int* MergeSort(int* arr, int n){

    if(n<=1)

        return arr;

    int half=n/2;

    int* L = new int[half];

    for(int i=0;i<half;i++){

        L[i] = arr[i];

    }

    int* R = new int[n-half];

    for(int i=0;i<n-half;i++){

        R[i]=arr[i+half];

    }

    L = MergeSort(L, half);

    R = MergeSort(R, n-half);

    return Merge(L,R,n);

}

int* Merge(int* L, int* R, int n){

    int* result = new int[n];

    int leftindex=0;

    int rightindex=0;

    for(int i=0;i<n;i++){

//        cout<<"Left: "<<L[leftindex]<<endl;

//        cout<<"Right: "<<R[rightindex]<<endl;

        if((L[leftindex]<=R[rightindex]||rightindex>=(n-(n/2)))&&leftindex<(n/2)){

//            cout<<"Left Smaller"<<endl;

            result[i] = L[leftindex];

            leftindex++;

        }

        else if((R[rightindex]<L[leftindex]||leftindex>=(n/2))&&rightindex<(n-(n/2))){

//            cout<<"Right Smaller"<<endl;

            result[i] = R[rightindex];

            rightindex++;

        }

//        cout<<result[i]<<endl;

    }

    return result;

}
```