
Finding the maximum subarray of a given array of integers; that is to say the subarray whose sum of all elements is largest.

Pseudocode:
```
FindMaximumSubarray(A, low, high)
	if high==low
		return(low,high,A[low])
	else
		mid=[low+high/2]
		(left-low,left-high,left-sum) = FindMaximumSubarray(A,low,mid)
		(right-low,right-high,right-sum) = FindMaximumSubarray(A,mid+1,high)
		(cross-low,cross-high,cross-sum) = FindMaxCrossingSubarray(A,low,mid,high)
		if(left-sum>=right-sum and left_sum>=cross-sum)
			return(left-low,left-high,left-sum)
		else if(right-sum>=left-sum and right-sum>=cross-sum)
			return(right-low,right-high,right-sum)
		else
			return(cross-low,cross-high,cross-sum)


FindMaxCrossingSubarray(A,low,mid,high)
	left-sum=-infinity
	sum=0
	for i=mid down to i=low
		sum+=A[i]
		if sum>left-sum
			left-sum=sum
			max-left=i
	right-sum=-infinity
	sum=0
	for j=mid up to i=high
		sum+=A[j]
		if sum>right-sum
		right-sum=sum
		max-right=j
	return(max-left, max-right,left-sum+right-sum)
```

For Lab03, below is a version in c++ that simply prints out the sum of that Max Subarray. If printing the pointers, or the entire arrays, etc is desired, only small tweaks are needed.

c++ implementation:
```
#include <iostream>

using namespace std;

int* FindMaximumSubarray(int* A, int low, int high);

int* FindMaxCrossingSubarray(int* A, int low, int mid, int high);

int main(){

    int length;

    cin>>length;

    int* arr = new int[length];

    for(int i=0;i<length;i++){

        cin>>arr[i];

    }

    int* result = new int[3];

    result=FindMaximumSubarray(arr,0,length-1);

    cout<<result[2];

    return 1;

}

  

int* FindMaximumSubarray(int* A, int low, int high){

    int* result = new int[3];

    if (high==low){

        result[0] = low;

        result [1]=high;

        result[2]=A[low];

        return(result);

    }

    else{

        int mid = (low+high)/2;

        int* left = FindMaximumSubarray(A,low,mid);

        int* right = FindMaximumSubarray(A,mid+1,high);

        int* cross = FindMaxCrossingSubarray(A,low,mid,high);

        if(left[2]>=right[2] && left[2]>=cross[2]){

            return left;

        }

        else if(right[2]>=left[2] && right[2]>=cross[2]){

            return right;

        }

        else{

            return cross;

        }

    }

}

  

int* FindMaxCrossingSubarray(int* A, int low, int mid, int high){

    int leftsum=A[mid];

    int sum = 0;

    int maxleft=mid;

    for(int i=mid;i>=low;i--){

        sum+=A[i];

        if(sum>leftsum){

            leftsum=sum;

            maxleft=i;

        }

    }

    int rightsum=A[mid+1];

    sum=0;

    int maxright=mid+1;

    for(int i=mid+1;i<high;i++){

        sum+=A[i];

        if(sum>rightsum){

            rightsum=sum;

            maxright=i;

        }

    }

    int* result = new int[3];

    result[0] = maxleft;

    result[1]=maxright;

    result[2]=leftsum+rightsum;

    return(result);

}
```