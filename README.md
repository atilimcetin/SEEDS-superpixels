# SEEDS Superpixels Wrapper for OpenCV
This is a simple OpenCV wrapper for original SEEDS superpixels implementation. It uses the 1.1 version at [authors website](http://www.mvdblive.org/seeds/).

## Example

```c++
cv::Mat image = cv::imread("star.png", cv::IMREAD_COLOR);

cv::Mat labels;
int count;
seeds(image, 2, 2, 4, labels, count);

cv::Mat contour;
labelContourMask(labels, contour, false);

image.setTo(cv::Scalar(255, 255, 255), contour);
```

[![Star](http://atilimcetin.com/SEEDS/star_small.png)](http://atilimcetin.com/SEEDS/star.png)
[![Star Labels](http://atilimcetin.com/SEEDS/star_labels_small.png)](http://atilimcetin.com/SEEDS/star_labels.png)


## License

Wrapper is MIT license. Please refer to [authors website](http://www.mvdblive.org/seeds/) for the license of original SEEDS superpixels implementation.
