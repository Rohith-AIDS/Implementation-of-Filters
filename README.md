# EX-06--Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import libraries and read the saved images using cv2.imread().

### Step2

Convert the saved BGR image to RGB using cvtColor().

### Step3

By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

### Step4

Apply the filters using cv2.filter2D() for each respective filters.

### Step5

Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

## Program: 
### Developed By   : SV ROHTIHKUMAR
### Register Number: 212221230084
</br>

### 1. Smoothing Filters

i) Using Averaging Filter

```Python
avg_filter = cv2.filter2D(image1,-1,kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")
```

ii) Using Weighted Averaging Filter

```Python
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(image1,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")
```

iii) Using Gaussian Filter

```Python
gaussian_blur = cv2.GaussianBlur(src = image1, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")
```

iv) Using Median Filter
```Python
median = cv2.medianBlur(src=image1,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")
```

### 2. Sharpening Filters

i) Using Laplacian Kernal

```Python
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(image1,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")
```

ii) Using Laplacian Operator

```Python
laplacian_operator = cv2.Laplacian(image1,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![image](https://user-images.githubusercontent.com/94980736/231580416-1f35e63f-5457-4460-ba45-466546f27a76.png)



ii) Using Weighted Averaging Filter
![image](https://user-images.githubusercontent.com/94980736/231580471-6b7577d4-3946-4ba9-968e-ae9518466c0f.png)



iii) Using Gaussian Filter
![image](https://user-images.githubusercontent.com/94980736/231580503-2107a2bd-9a09-4c00-a418-7fd555638b8f.png)



iv) Using Median Filter
![image](https://user-images.githubusercontent.com/94980736/231580540-2fb8a505-4056-4772-a448-a62133ad77b8.png)


### 2. Sharpening Filters
</br>


i) Using Laplacian Kernal
![image](https://user-images.githubusercontent.com/94980736/231580588-ce912e4c-ad93-420a-a8ca-3468f4464029.png)



ii) Using Laplacian Operator

![image](https://user-images.githubusercontent.com/94980736/231580636-19ef3c04-3f50-48ad-8913-72224d9ffacb.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
