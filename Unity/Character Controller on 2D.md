1. Character Controller 충돌 체크
a. Chracter Controller에서 Move 함수를 이용해 이동시
자동으로 Collision체크를 해서 OnControllerColliderHit가 호출되는게 정상이나 
Collision들이 2D일 경우에는 작동을 하지 않음.

2. skin width
맵의 바닥의 컬리젼들을 각각의 BoxCollision 들을 붙여놓은 형태로 제작했는데
Rigidbody 2d를 적용했을 때 컬리젼의 겉 부분이 완벽한 사각형일 때 BoxCollision사이에
틈이 있는 것처럼 끼어서 못 움직이니는 현상이 있었다. (이럴 경우는 겉에 Radius 값을 줘서 둥그렇게 만들면 지나갈 순 있으나 어색)

Character Controller에선 이런 현상을 skin width 값을 조절해서 약간의 여유 공간을 주는 것으로 해결했다.
