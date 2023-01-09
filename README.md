# TIL010
## 판다스 활용
* import pandas as pd
import numpy as np
* result = emp.groupby('job')['sal'].max().reset_index()
* result = pd.merge(emp, dept, on = 'deptno')

***

## 시각화
* import matplotlib.pyplot as plt
import numpy as np
%matplotlib inline  # plt 객체를 통해 그래프를 show() 렌더링, 대신에 사용