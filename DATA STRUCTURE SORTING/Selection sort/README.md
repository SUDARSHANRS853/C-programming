Here there is selection sort
```
for(i=0;i<n;i++)
{
 int min=i;
 for(j=i+1;j<n;j++)
      {
        if(a[j]<a[min])
          {
          min=j;
          }
       }
  if(min!=i)
      {
        swap(a[i],a[min]);
      }
}
```

