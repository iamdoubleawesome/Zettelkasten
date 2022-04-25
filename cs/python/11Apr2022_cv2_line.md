#11Apr2022

# `cv2.line`

```python
cv2.line(image, pt1, pt2, color, thickness, lineType, shift)
```

- `image`:` <class 'numpy.ndarray'>`
- `pt1`, `pt2`: `(x, y)` in absolute pixel value, 0 starts from left upper corner; start and end point for the line segment
- `color`: `cv2` uses`BGR`, so `(255, 0, 0)` is blue
- `thickness`:  in pixels
- `lineType`: default `cv2.LINE_8`, can found choices from [11Apr2022_cv2_linetype](11Apr2022_cv2_linetype)
- Return a `<class 'numpy.ndarray'>` which modifies the input image



---

#cv2 #opencv #line #drawing

---

Source:

- https://www.geeksforgeeks.org/python-opencv-cv2-line-method/
