A sorting algorithm which uses the heap data structure, rearranging the data into a binary tree where no child is larger than its parent. This one is a lot to wrap my head around, honestly.
It runs in $O(nlogn)$ time complexity, and it sorts in-place, allocating no additional memory.
See page 151 in the textbook(which is 172 in the pdf) for a full explanation.

c++ implementation:
```
#include<iostream>

using namespace std;

int Parent(int i){

    return (i/2);

}

int Left(int i){

    return (i*2);

}

int Right(int i){

    return ((i*2)+1);

}

void Heapify(int* arr,int length, int index){

    int max = index;

    int l = Left(index);

    int r = Right(index);

    if(l<length && arr[l]>arr[max]){

        max=l;

    }

    if(r<length && arr[r]>arr[max]){

        max=r;

    }

    if(max!=index){

        int placeholder = arr[index];

        arr[index]=arr[max];

        arr[max]=placeholder;

        Heapify(arr,length,max);

    }

}

void HeapSort(int* arr, int length){

    for(int i = ((length/2)-1);i>=0;i--){

        Heapify(arr, length, i);

    }

    for(int i=length-1;i>0;i--){

        int placeholder=arr[0];

        arr[0]=arr[i];

        arr[i]=placeholder;

        Heapify(arr,i,0);

    }

}

int main(){

    int length;

    cin>>length;

    int* arr = new int[length];

    for(int i=0;i<length;i++){

        cin>>arr[i];

    }

    HeapSort(arr,length);

    for(int i=0;i<length;i++){

        cout<<arr[i]<<";";

    }

    return 1;

}
```