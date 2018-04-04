RaycastHit2D hit = Physics2D.Raycast(new Vector2(transform.position.x, transform.position.y), direction, distance, 1 << LayerMask.NameToLayer("Layer");

레이어마스크는 별도의 할당된 순서가 있긴 하지만
이게 유니티상에서는 비트의 위치를 뜻함
(각 비트위치의 1,0값으로 enable, disable을 구분)
(왜 처음에 레이어마스크를 할당해줄때는 그냥 일반 숫자값을 넣어줘도 되는지는 의문)
이렇게 해줘야 작동함.