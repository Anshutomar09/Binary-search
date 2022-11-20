# Binary-search
//binary search............

#include <iostream>
using namespace std;

int binarysearch(int arr[], int n , int key){
    int start=0;
    int end= n-1;
    int mid= (start+end)/2;
    while(start<=end){
    if(arr[mid]==key){
        return mid;
    }
    if(arr[mid]<key){
        start=mid+1;
    }
    else{
        end=mid-1;
    }
    mid=(start+end)/2;
}
return -1;
}
int main()
{
    int even[5]={2,4,8,10,12};
    int odd[4]={3,5,7,9};
    cout<<"index of 4 is "<<binarysearch(even,5,4);
    

    return 0;
}
