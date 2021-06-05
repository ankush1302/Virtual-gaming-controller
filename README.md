# Virtual-gaming-controller

The whole project is divided into three parts :
1. Color Detection
2. capturing movement/position of that color capturing contour (box)
3. Automate the keyboard keys using pyautogui (*pyDirectInput* for key control in games)

## Color Detection 

1. Converted the imageFrame in BGR to HSV(hue-saturation-value) color space. **HSV** can be represented as three matrices in the range of 0-179, 0-255 and 0-255 respectively.
2. Defined the range of color and create the corresponding mask.
3. **Dilation** is done to remove noises from the images.
4. **bitwise_and** is used between the image frame and mask to specificaly detect that particular color and discrad others.
5. Created contour or region for the individual colors to display the detected colored region distinguishly.

for HSV color range : ![hsv](https://user-images.githubusercontent.com/52347680/120885121-e9d2b080-c604-11eb-8a55-74227a5128cb.png)

## capturing movement and position

1. mid point of whole capturing window is taken and mid point of color capturing contour is taken => slope is calculated 
2. angle is calculated with horizontal for movement calculation

![pic1](https://user-images.githubusercontent.com/52347680/120885494-ef30fa80-c606-11eb-82ca-f0a6bdb1465c.png)


## Automate the keyboard keys using pyautogui (*pyDirectInput* for key control in games)

1. Using pyautogui , keyboard keys get controlled according to our contour movement 

2. But sometimes pyautogui does not work in games , so additionally , pydirectinput is used for same

**All key-control and movement capuring can be customised as per our game requiremnt**


![pic2](https://user-images.githubusercontent.com/52347680/120885641-96159680-c607-11eb-8fd6-3952a16a43de.png)



