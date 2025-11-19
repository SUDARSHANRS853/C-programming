Here is the Merge sort
```
MergeSort(A, lb, ub)
{
    if(lb < ub)
    {
        mid = (lb + ub) / 2;

        MergeSort(A, lb, mid);        // Left half
        MergeSort(A, mid + 1, ub);    // Right half

        Merge(A, lb, mid, ub);        // Combine
    }
}

Merge(A, lb, mid, ub)
{
    i = lb;
    j = mid + 1;
    k = lb;

    while(i <= mid && j <= ub)
    {
        if(A[i] <= A[j])
        {
            B[k] = A[i];
            i++;
        }
        else
        {
            B[k] = A[j];
            j++;
        }
        k++;
    }

    while(i <= mid)        // Copy remaining left half
    {
        B[k] = A[i];
        i++;
        k++;
    }

    while(j <= ub)         // Copy remaining right half
    {
        B[k] = A[j];
        j++;
        k++;
    }

    // Copy B back into A
    for(x = lb; x <= ub; x++)
        A[x] = B[x];
}

```

