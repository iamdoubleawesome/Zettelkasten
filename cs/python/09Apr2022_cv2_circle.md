#09Apr2022

# `cv2.circle`

```python
cv2.circle(image, center_coordinates, radius, color, thickness, lineType, shift)
```

- `image`:` <class 'numpy.ndarray'>`
- `centre_coordinates`: `(x, y)` in absolute pixel value, 0 starts from left upper corner
- `radius`: radius of circle in pixel
- `color`: `cv2` uses`BGR`, so `(255, 0, 0)` is blue
- `thickness`: circle border line in pixels, and `-1` fills circle
- `lineType`: default `cv2.LINE_8`, can found choices from [11Apr2022_cv2_linetype](11Apr2022_cv2_linetype)
- Return a `<class 'numpy.ndarray'>` which modifies the input image



---

#cv2 #opencv #circle #drawing

---

Source:

- https://www.geeksforgeeks.org/python-opencv-cv2-circle-method/
- https://docs.opencv.org/4.x/d6/d6e/group__imgproc__draw.html#gaf10604b069374903dbd0f0488cb43670

