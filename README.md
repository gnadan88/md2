# State Variable

## **The concept of State Variable**
* state = system의 내부상태
* 문제를 푸는 과정에 의미부여
* 컴퓨터에게 일을 시키기 쉽게 식을 바꿔나가는 과정

![이미지설명문구](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FOMCZ6%2Fbtqu6AFzhki%2FvnMiaHyThL2w4PpqEKxxwk%2Fimg.png)

* 출력 y(t)는 입력u(t)가 system의 상태 x(t)를 통과하여 생기는 결과값이다.

### <Example: spring-mass-damper system>

$M\frac{d^2y(t)}{dt^2}\+b\frac{dy(t)}{dt}\+ky(t)=r(t)$

state 설정  
>$x_1(t)=y(t)$  
$x_2(t)=\frac{dy(t)}{dt}$

2차 미분방정식을 2개의 1차 미분방정식으로 변환  
>$\frac{dx_1(t)}{dt}\=x_2(t)$  
$\frac{dx_2(t)}{dt}\=\frac{-b}{M}x_2(t)+\frac{-k}{M}x_1(t)+\frac{1}{M}r(t)$

## **State Vector**

$$\begin{equation*}
x(t) = 
\begin{pmatrix}
x_1(t) \\
x_2(t) \\
\vdots\\
x_n(t) 
\end{pmatrix}
\end{equation*}$$

## State space equation
### **state differential equation**  
차 미분방정식을 여러 개의 1차 미분방정식으로 바꿔 1차 행렬 미분방정식으로 변환
>$\dot{\mathbf{x}}(t)=\mathbf{A}\mathbf{x}(t)+\mathbf{B}\mathbf{u}(t)$

### **output equation**  
state들과 input을 조합한 output
>$\mathbf{y}(t)=\mathbf{C}\mathbf{x}(t)+\mathbf{D}\mathbf{u}(t)$

위 두식을 묶어서 state space equation이라 함. 즉 최초의 미분방정식을 state space equation으로 바꾸는 것이라 할 수 있다. 이를 통해 의미파악이 가능하고 컴퓨터에게 일을 시키기 쉬워짐.  

## State transition matrix
$\mathbf{x}(t)=\Phi(t)\cdot\mathbf{x}(0)+\int{\Phi(t-\tau)\mathbf{b}\mathbf{u}(\tau)d\tau}$
