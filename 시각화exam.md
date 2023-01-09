# 시각화 예제
* 모듈 및 데이터 불러오기
> * import pandas as pd
> * import matplotlib.pyplot as plt
> * emp = pd.read_csv('C:/ds_work/data/emp.csv')

***

## exam01. 
* emp.csv 를 로드한 후 이름과 봉급을 기점으로 선 그래프를 그린다.
> * plt.plot(emp.ename, emp.sal)
> * plt.xlabel('ename') 
> * plt.ylabel('sal')
> * plt.show()
## exam02.
* 직업별로 봉급을 그룹화 한 결과를 원 그래프를 그려서 수치를 범례표시한다.
> * s1 = emp.groupby('job')['sal'].sum().reset_index()
> * plt.pie(s1.sal, labels=s1.job, autopct='%.1f%%')
> * plt.show()
## exam03.
* 부서별 결과를 막대그래프로 표시한다. 단, 봉급의 합을 이용한다.
> * s1 = emp.groupby('deptno')['sal'].sum().reset_index()
> * plt.bar( s1.deptno, s1.sal) 
> * plt.xlabel('deptno') 
> * plt.ylabel('sum(sal)')
> * plt.show()
## exam04.
* 직업별, 부서별 봉급의 최대값을 두개의 곡선으로 그려낸다.
> * s1 = emp.groupby('job')['sal'].max().reset_index()
> * s2 = emp.groupby('deptno')['sal'].max().reset_index()
> * plt.plot(s1.job, s1.sal)
> * plt.plot(s2.deptno, s2.sal)
> * plt.show()