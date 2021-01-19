# 2 Optimization VS Illumination Algorithms
Optimization : best solution을 찾을 때도 있지만, 항상 그런 것은 아니다.
Illumination : phenotype-fitness map(fitness map 표현형)을비춘다(Illumination)
-> Optimization의 super set 개념이다.

MAP-Elites는 세가지 Illumination Algorithms에 영향을 받았다.
(Novelty Search + Local Competition + Multi-Objective Landscape Exploration algorithm)

# 3 Details of the MAP-Elite algorithm
1. perfomance measure f(x)를 정의 (fitness function)
2. interest dimension of variation을 정의
3. dimension of vaiation의 변수들을 이산화(discretization)한다.
4. 각각 이산화 된 cell에서 best solution을 각각 찾는다.

b(x)는 solution에 대해서 interest feature를 뽑아내는 역할을 한다.
이 것이 필요한 이유는 energy consuming per second 처럼 direct하게 알 수 없는 feature들이 있기 때문이다.
-> 특히 indirect encoding이 그러하다.

terminate criteria는 다양하다.
그 중 매력적인 condition은 map cell이 일정수준 이상으로 채워지는 것,
평균 fitness가 특정 수준을 넘어가는 것,
몇가지 best solution들이 나오는 것이다.

multithreading 같은 것을 활용하여 large cell에서 predetermined 된 값을 
small cell에서 parallel하게 돌릴 수 있다.

주의해야 할 점 :
1. 모든 cell을 전부 커버하지 못할 수 있다.
2. 완전 탐색 VS perfomance 의 trade offf를 고려하라

# 7 Discussion and Conclusion
아무튼 MAP-Elite가 좋더라~ 이말이야~

MAP-Elite는map을 밝혀주기에, feature간의 상관관계를 판단하기 용이하다.
MAP-Elite는 새로운 cell을 추가할 수 없기에 open-ended evolution을 만들 수 없다.
