# PythonProject

import cv2
# 摄像头捕捉
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    # 边缘检测（Canny算法）
    edges = cv2.Canny(frame, 100, 130)
    cv2.imshow('Original', frame)
    cv2.imshow('Edges', edges)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
