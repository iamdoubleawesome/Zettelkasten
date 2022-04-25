#11Apr2022

# `cv2.rectangle`

```python
cv2.rectangle(image, pt1, pt2, color, thickness)
```

- `image`:` <class 'numpy.ndarray'>`
- `pt1`, `pt2`: `(x, y)` in absolute pixel value, 0 starts from left upper corner; `pt1` is the left upper corner and `pt2` is right bottom corner
- `color`: `cv2` uses`BGR`, so `(255, 0, 0)` is blue
- `thickness`:  in pixels
- `lineType`: default `cv2.LINE_8`, can found choices from [11Apr2022_cv2_linetype](11Apr2022_cv2_linetype)
- Return a `<class 'numpy.ndarray'>` which modifies the input image



---

#cv2 #opencv #rectangle #drawing

---

Source:

- https://shikaku-mafia.com/opencv-rectangle/
