---
title: "What Is Bits"
date: 2020-04-22T18:23:43+09:00
categories: ["CS"]
tags: ["whatis"]
cover: ""

---
## Bits ?

> Bits는 0혹은 1의 나열이다.

- 컴퓨터 과학에서는 데이터(상태, 값 등)들을 0혹은 1의 나열로 표현한다.
- 즉, 2진수로 모든 데이터(상태, 값 등)들을 표현한다는 것이다.
- N bits로 N^2^ 가지의 데이터를 표현할 수 있다.

## 그래서 뭐?
- 사실 누구나 다 아는 사실이었을 것이다.
- 그럼 밑의 문제를 풀 수 있나 확인해보자.

## 문제
> 1000병의 와인이 있고 그 중 1병의 와인에 독이 들어있다.  
당신은 한 시간 뒤에 파티가 열리기 전에 그 독이 든 와인 1병을 찾아야 한다.  
다행히 당신에게는 테스트 할 10마리의 쥐가 있다.  
쥐에게 독이 든 와인을 먹이면 한 시간 뒤에 약효가 발휘되어 쥐가 죽게 된다.  
한 시간 뒤에 파티가 열리므로 결과를 한 번 보고 또 실험 할 수 없다.  
즉, 기회는 한 번 뿐이다. 어떻게 해야할까?  
(쥐에게 독이 든 와인을 한 방울만 먹여도 약효가 나타난다.)  

## 풀이 1 (잘못된 풀이)
처음에 쉽게 생각할 수 있는 것은 하나의 쥐에게 한 병의 와인을 매칭시켜서 먹이는 것이다.  
그런데 그렇게 하면 10 병의 와인 밖에 확인을 못한다.

## 풀이 2 (잘못된 풀이)
그다음 쉽게 생각 할 수 있는 것은 하나의 쥐에게 100병의 와인을 매칭시켜 먹이고 죽은 쥐와 매칭된 100병의 와인을 다 버리는 것이다.   
이렇게 하면 풀이 1 보다는 낫지만 정확히 1병의 독이든 와인을 찾지 못하여 나머지 99병의 와인을 낭비하게 된다.  

그럼 어떡해야할까?

----

## 풀이 3 (올바른 풀이)
이 글의 주제인 bits를 이용하는 것이다.  
앞에서 컴퓨터는 값이나 상태를 bits로 표현한다고 했다.  
쥐 10 마리를 선택하는 패턴은 1024가지이다.  
즉, 쥐 10마리로 만들수 있는 표현이 1024가지라는 것이다.

- 각 와인과 쥐를 1열로 세우고
- 쥐를 선택하는 각각의 패턴들(1000가지) 마다 와인 한 병과 매칭시킨다.
- 한 시간 뒤, 죽은 쥐들을 보고 그 패턴이 어떤 와인과 매칭됐었는지 확인하면 독이든 한 병의 와인을 특정지을수있다.