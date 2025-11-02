Here is the Insertion sort
```
for(i=1;i<n;i++)
  {
  j=i-1;
  temp=a[i];
  while(j>=0 &&a[j]>temp)
    {
      a[j+1]=a[j];
      j--;
    }
  a[j+1]=temp;
  }
```
