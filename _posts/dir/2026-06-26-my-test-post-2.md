---
layout: post
title: "My Test Post 2"
date: 2026-06-26 08:50:31 +0530
categories: jekyll Cat2
author: "Shubham"
---

# Hello World

Some Content

## Hello world 2

```python
print("Hello World")
```

```c
long long countMajoritySubarrays(int* nums, int numsSize, int target) {
    int n = numsSize;
    long long cnt = 0;

    for (int i = 0; i < n; i++) {
        if (nums[i] == target)
            nums[i] = 1;
        else
            nums[i] = -1;
    }

    int* pref = (int*)malloc(sizeof(int) * n);
    pref[0] = nums[0];

    for (int i = 1; i < n; i++) {
        pref[i] = pref[i - 1] + nums[i];
    }

    int shift = n;
    int* freq = (int*)calloc(2 * n + 1, sizeof(int));

    freq[shift] = 1;

    long long valid = 0;
    int lastSum = 0;

    for (int i = 0; i < n; i++) {
        if (pref[i] > lastSum) {
            valid += freq[lastSum + shift];
        } else {
            valid -= freq[pref[i] + shift];
        }

        cnt += valid;
        freq[pref[i] + shift]++;
        lastSum = pref[i];
    }

    free(pref);
    free(freq);

    return cnt;
}
```

### Hello World 3

#### Hello World 4
