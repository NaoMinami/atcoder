# atcoder memo

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

## 二分探索

int数列arrの中から、keyの値を探索する二分探索法
```c++
int binary_search(int arr[], int key)
{
    int left = -1;
    int arr_len = sizeof(arr) / sizeof(arr[0]);
    int right = arr_len - 1;
    while (right - left > 1)
    {
        int mid = left + (right - left) / 2;
        if (key == arr[mid]) return mid;
        else if (key < arr[mid]) right = mid;
        else if (key > arr[mid]) left = mid;
    }
    if (key == arr[right]) return right;
    return -1;
}
```

