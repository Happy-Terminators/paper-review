# 1 Introduction
Authority Layer / Meta Layer / Tactical Layer 3가지로 분류가 가능하다.
1. Authority Layer : new cards, change rules, New play mechine, Tweak Cards
   Tweak Cards를 "카드 밸런싱"이라고 볼 수 있다.

2. Meta Layer : Emergence and extinction of popular archetypes and tatics
   게임의 메타는 Authority Layer에서 일어나는 변경사항으로 인해 생겨나기도, 없어지기도 한다.
   밸런싱을  Meta 변경을 예상하면서 진행하는 것이 적절할 것이다. 하지만 어떻게?

3. Tactical Layer : Game play, deck construction-experiment
   실제 게임을 플레이하고 연습하는 단계이다.

## 1.1 past research
하스스톤 기준으로, evolutionary algorithm을 사용하여 deck을 만들어 유의미한 win-rate상승을 보여준 연구,  
AI로 덱을 만다는 연구,  
상대방의 움직임을 95%의 확률로 예측하는 algorithm을만든 연구가 있었다.  
특히, 마지막 연구는 게임이 break 될 것을 우려하여 그 algorithm을 공개하지 말것을 요구받았다.  
개인적으로 상당히 흥미롭다.   
게임을 터트려버릴 정도의 연구 결과가 나오는게 가능이나 한 이야기인가?  

utility system을 사용하여 deck을 cost efficiency, card synergy를 고려하여 짜는 연구도 있다.  
유명한 archetypes에 따라 deck 스켈레톤을 짜는 연구,  

등등등 많은 연구들이 있다. 여기서 언급되는 논문들만 다시 살펴봐도 크게 도움이 될 듯하다.

## 1.2 Intent of this work
게임 publisher의 행동이 player들의 decision-making에 어떤 영향을 주는지에 대한 연구이다.  
Hearthstone의 역사를 Information-theoretic measures로 측정을 한 일종의 역사적인 연구인 것이다.  

## 1.4 Archetypes and character classes
* Aggro archetypes : low mana cost로 deck을 구성하여 early stage에 상대방을 끝내버리는 전략
* Control archetypes : high mana cost, high value(health, attack) 카드로 deck을 구성하여 조금더 later stage까지 생각하는 전략
* Combo archetypes : 카드간의synergy에 의존하는 덱. 콤보로 상대를 일찍 끝내려고 하지만, high mana cost, high value카드들도 역시 사용한다. 

## 1.5 Information-theoretic measures
Shannon entropy, Bayes\` thoerem 등을 사용한다.

# 2 Data explanation and explanation
유의미 하게 응용 가능할 것으로 여겨지는 몇가지 수식을 소개하겠다.

<img src="https://latex.codecogs.com/svg.latex?\Large&space;x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" title="\Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" />

h<sub>&theta;</sub>(x) = &theta;<sub>o</sub> x + &theta;<sub>1</sub>x