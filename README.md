# Calculate_Similarity
This repository contains code to evaluate the similarity between two images based on their histograms.

By comparing the histograms, we can gauge how visually similar two images are in terms of color distribution and intensity. This method is particularly useful in image retrieval, image matching, and various computer vision tasks where understanding the similarity between images is crucial.

<br>

## Features:

- Computes histograms for input images.
- Compares histograms using various metrics (e.g., Chi-Square, Correlation).
- Provides a similarity score indicating how alike the two images are.

Ideal for researchers, developers, and hobbyists looking to understand and implement histogram-based image comparison in their projects.

<br>

## About cv2.compareHist()
cv2.compareHist() is a function provided by OpenCV that is used to compare the similarity between two histograms. 

This function supports various comparison methods, 

and here, we will explain two methods: __HISTCMP_CORREL__ and __HISTCMP_CHISQR__.

<br>

### HISTCMP_CORREL (Correlation)

This method measures the correlation between two histograms.

The return value ranges from -1 to 1.

A value closer to 1 indicates that the two histograms are very similar, while a value closer to -1 indicates that they are very different.

A value of 0 indicates no correlation between the two histograms.

<br>

### HISTCMP_CHISQR (Chi-Square)

This method calculates the chi-square distance between two histograms.

The return value ranges from 0 to infinity.

A value of 0 indicates that the two histograms are identical, and as the value increases, it indicates that the histograms are different.

In summary, HISTCMP_CORREL is used to measure the similarity between two histograms, while HISTCMP_CHISQR is used to measure the difference between them.

<br>

## Examples:
Image 1 is from [CelebAMask-HQ](https://github.com/switchablenorms/CelebAMask-HQ).
Image 2, represents Image 1 with a rendered mask, is made by our algorithm.

- Image 1

![00256](https://github.com/Seungeun-Han/Calculate_Similarity/assets/101082685/4d155f14-49f7-42e4-a726-be2a37e5196b)

- Image 2

![00256_kf94](https://github.com/Seungeun-Han/Calculate_Similarity/assets/101082685/8e829500-1a62-406d-b937-ab8560168bb5)

- OutPut

```
Similarity_by_CORREL: 0.964484452431569
Similarity_by_CHISQR: 20.198742090646427
```

HISTCMP Correlation 이 1에 가까운 것으로 보아 두 사진은 유사하다고 말할 수 있다.

  
