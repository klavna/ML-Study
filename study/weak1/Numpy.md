# Numpy

## Numpt 기초 사용법
- `numpy` 를 inport해오서 사용 할 때 `np`로 쓰겠다
```
 import numpy as np
```
- 슬라이싱 예제
```
arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])
print(arr[0:2, 1:4
```
### 데이터 타입
> i - integer <br>
> b - boolean <br>
> u - unsigned integr<br>
> f - float<br>
> c - complex float<br>
> m - timedelta<br>
> M - datetime<br>
> O - object<br>
> S - string<br>
> U - unicode string<br>
> V - fixed chunk of memory for other type <br>
`dtype`는 array의 형을 알려준다. `astype()`은 array를 복사해와 형을 변환한다.

### copy vs view
  - `copy()`는 새로운 데이터를 만들고 원본과는 상관이없다.
  - `view()`는 데이터 타입이 아니고 view를 수정하면 원본도 수정된다
```
모든 NumPy 배열에는 배열이 데이터를 소유하는 경우 None을 반환하는 속성 기반이 있습니다.
그렇지 않으면 기본 속성이 원래 개체를 참조합니다.
```
### Array Shape
  - `.shape`이라는 각각의 index 요소를 튜플형식으로 전해주는 속성이 있다.
  예)  
```
arr = np.array([1, 2, 3, 4], ndmin=5)
print(arr)
print('shape of array :', arr.shape)
```
'ndmin'은 차원수를 정함
'reshape()'은 array의 모양을 재정의 view()형식임

### Array Lterating 

`np.nditer()`배열의 차원 상관없이 반복 할 수 있다.
`np.nditer()` 다른 데이터 유형으로 배열 반복하기 op_dtypes 인수를 사용하고 반복하는 동안 요소의 데이터 유형을 변경하고 데이터 유형을 전달할 수 있습니다.
```
for x in np.nditer(arr, flags=['buffered'], op_dtypes=['S']):
  print(x)
```
이해가 가지 않는다.
```
for x in np.nditer(arr[:, ::2]):
  print(x)
```
`np.ndenumerate()`는 인덱스 번호가 필요할 때 사용한다.
```
for idx, x in np.ndenumerate(arr):
  print(idx, x) 
```

