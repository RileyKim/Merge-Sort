##1. 합병정렬/병합정렬 (Merge Sort)



**합병정렬은
전체 원소를 하나의 단위로 분할한 후 분할한 원소를 다시 병합하는 정렬 방식입니다.**



아래 예제를 통해 합병정렬이 어떤것인지 알 수 있을 겁니다. 


![예시1](https://github.com/Taeksu89/Merge-Sort/blob/master/image01.gif ) {.aligncenter}






**합병정렬의 과정**

![예시2](https://github.com/Taeksu89/Merge-Sort/blob/master/image02.png ) {.aligncenter}



1. 리스트의 길이가 1이 될때까지 반으로 잘게 나눈다.-> 분할(Divide)

![예시3](https://github.com/Taeksu89/Merge-Sort/blob/master/image03.png) {.aligncenter}

![예시4](https://github.com/Taeksu89/Merge-Sort/blob/master/image04.png) {.aligncenter}


2. 다 나누어 졌다면, 데이터를 합치는데(Merge), 정렬하면서 합친다. 

(작은 숫자를 앞에놓고 큰 숫자를 뒤에 놓는다)



자 저희가 쪼갠 데이터중 제일 앞 두개를 가져와봤어요.

![예시5](https://github.com/Taeksu89/Merge-Sort/blob/master/image05.png) {.aligncenter}

데이터를 합치는데 정렬하면서 합친다!

5와 6을 비교하여 작은것은 앞에, 큰것은 뒤에 놓으면 되겠죠?

결과적으로, 

![예시6](https://github.com/Taeksu89/Merge-Sort/blob/master/image06.png) {.aligncenter}


이렇게 되는 것입니다. 

이 과정을 반복하면 결과는 이렇게 나옵니다.

![예시7](https://github.com/Taeksu89/Merge-Sort/blob/master/image07.png) {.aligncenter}




이제 가장 흥미진진한 시간인 시간복잡도를 계산해보겠습니다.



먼저 크기가 N인 배열을 반으로 쪼개면서 분할해 나가죠? 

한번 분할하면 N/2, N/2 -> 2개가 생기고,

그다음 분할하면 N/4,N/4,N/4,N/4 -> 4개

.

.

우리는 크기가 8인 배열로 예를 들었습니다.

최종적으로 N/8짜리가 8개 생겼었어요. 

그리고, 3번만에 길이가 1인 배열을 만들어 냈다는 겁니다.



즉. 분할과정은 매번 반씩 감소하므로

밑이 2인 logN만큼 반복해야 크기가 1인 배열로 분할 할 수 있습니다.

각 분할별로 합병을 진행하므로

합병정렬의 시간복잡도는

O(NlogN)입니다. 



병합정렬은 최악의 경우에도 O(nlogn)의 시간복잡도를 가진다는 것입니다.



