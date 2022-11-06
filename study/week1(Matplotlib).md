# Matplotlib
`Matplotlib`는 시각화 유틸리티 역할을 하는 파이썬의 저수준 그래프 플로팅 라이브러리이다.

### Plotting
`plot()` 함수는 다이어그램에서 점(마커)을 그리는 데 사용됩니다.
기본적으로 plot() 함수는 점에서 점으로 선을 그립니다.
```python
xpoints = np.array([1, 2, 6, 8])
ypoints = np.array([3, 8, 1, 10])

plt.plot(xpoints, ypoints)
plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200181906-be559965-d339-40b2-a71f-8260d44b8db6.png)

### Markers
키워드 `markers` 이용하여 포인트를 줄수있다.
```python
ypoints = np.array([3, 8, 1, 10])
plt.plot(ypoints, marker = 'o', ms = 20, mec = 'r', mfc = 'b')
plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200183794-61fe5f74-0729-4449-9762-635c3c573d89.png)

### Labels
Pyplot에서는 `xlabel()` 및 `ylabel()` 함수를 사용하여 x축 및 y축에 대한 레이블을 설정할 수 있습니다.
```python
x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

font1 = {'family':'serif','color':'blue','size':20}
font2 = {'family':'serif','color':'darkred','size':15}

plt.title("Sports Watch Data", fontdict = font1, loc='left')
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y)
plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200181868-38f8e195-c6bf-413b-bf69-0d24e98136c0.png)

### Grid
```python
x = np.array([80, 85, 90, 95, 100, 105, 110, 115, 120, 125])
y = np.array([240, 250, 260, 270, 280, 290, 300, 310, 320, 330])

plt.title("Sports Watch Data")
plt.xlabel("Average Pulse")
plt.ylabel("Calorie Burnage")

plt.plot(x, y)

plt.grid(color = 'green', linestyle = '--', linewidth = 0.5)

plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200182083-a082c08a-0b01-4585-91b2-7660122a1da2.png)

### subplot
```python
x = np.array([0, 1, 2, 3])
y = np.array([3, 8, 1, 10])

plt.subplot(3, 3, 1)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([10, 20, 30, 40])

plt.subplot(3, 3, 2)
plt.plot(x,y)

x = np.array([0, 1, 2, 3])
y = np.array([10, 21, 34, 47])

plt.subplot(3, 3, 3)
plt.plot(x,y)
x = np.array([0, 1, 2, 3])
y = np.array([10, 21, 34, 47])

plt.subplot(3, 3, 4)
plt.plot(x,y)
x = np.array([0, 1, 2, 3])
y = np.array([10, 21, 34, 47])

plt.subplot(3, 3, 5)
plt.plot(x,y)
x = np.array([0, 1, 2, 3])
y = np.array([10, 21, 34, 47])

plt.subplot(3, 3, 6)
plt.plot(x,y)
x = np.array([0, 1, 2, 3])
y = np.array([10, 21, 34, 47])

plt.subplot(3, 3, 7)
plt.plot(x,y)
plt.suptitle("test")
plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200182533-297a31e5-5885-4b3e-9fc1-1127f3cdbe3c.png)

### Scattter
`scatter()` 함수는 대해 하나의 점을 표시합니다. 동일한 길이의 배열 두 개가 필요합니다. 하나는 x축이고 다른 하나는 y축입니다.
```python
x = np.array([5,7,8,7,2,17,2,9,4,11,12,9,6])
y = np.array([99,86,87,88,111,86,103,87,94,78,77,85,86])
colors = np.array([0, 10, 20, 30, 40, 45, 50, 55, 60, 70, 80, 90, 100])

plt.scatter(x, y, c=colors, cmap='viridis')
plt.colorbar()
plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200182862-05b8258a-a334-428e-9d56-801b693f7070.png)

### Bars
`bar()`로 바그래프를 나타낸다
```python
x = np.array(["A", "B", "C", "D"])
y = np.array([3, 8, 1, 10])

plt.bar(x, y, width = 0.5,color="blue")
plt.show()
```
![image](https://user-images.githubusercontent.com/100742454/200183089-6175319e-f268-4eac-b71d-e5e296b6d979.png)

### Histogram
`hist()` 함수를 사용하여 히스토그램을 만듭니다.
`hist()` 함수는 숫자 배열을 사용하여 히스토그램을 만들고 배열이 인수로 함수에 전송됩니다.

### Pie Charts
`Pie()`를 이용하여 파이차트를 나타낸다.
```python
y = np.array([35, 25, 25, 15])
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]
myexplode = [0.2, 0, 0, 0]
mycolors = ["m", "hotpink", "y", "#4CAF50"]

plt.pie(y, labels = mylabels, explode = myexplode, shadow = True, startangle = 90, colors = mycolors)
plt.legend(title= "Four Fruits:",loc = 'right')
plt.show() 
```
![image](https://user-images.githubusercontent.com/100742454/200183715-20398133-bddd-4ebf-acd2-258b266a7c3d.png)
