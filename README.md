# SEEDS Superpixels Wrapper for OpenCV
This is a simple OpenCV wrapper for original SEEDS superpixels implementation. It uses the 1.1 version at [authors website](http://www.mvdblive.org/seeds/).

## Example

```c++
cv::Mat image = cv::imread("image.png", cv::IMREAD_COLOR);

cv::Mat labels;
int count;
seeds(image, 2, 2, 4, labels, count);

cv::Mat contour;
labelContourMask(labels, contour, false);

image.setTo(cv::Scalar(0, 0, 255), contour);

cv::imshow("SEEDS", image);
cv::waitKey(0);
```

## License

Wrapper is MIT license. Please refer to [authors website](http://www.mvdblive.org/seeds/) for the license of original SEEDS superpixels implementation.
