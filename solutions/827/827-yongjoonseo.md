# 827. Making A Large Island

## solution 1

시간복잡도 : O(N^2)

알고리즘 : Union-Find, BFS

풀이 설명 : `grid`가 1인 지점에서 BFS를 시행합니다. 탐색을 하면서 방문처리를 해주고 union연산도 함께 해줍니다. BFS가 실행될 때마다 총 방문한 지점 수를 반환하여 `(방문 시작 지점): (총 방문한 지점 수)`와 같이 딕셔너리에 저장합니다. `grid`가 0인 지점은 별도의 리스트에 저장합니다(`zeros`). 만약 `zeros`에 요소가 있다면 해당 지점의 위, 아래, 왼쪽, 오른쪽 위치로 find 연산을 해서 서로 다른 섬의 크기를 모두 더해 결과값과 비교하여 더 큰 값으로 갱신하며 `zeros` 배열을 순회합니다. 순회가 완료되면 최종적으로 갱신된 결과값을 반환합니다. `zeros`에 요소가 없다면 딕셔너리의 `(0, 0)` 키에 저장된 값을 반환합니다.

소스코드 : [link](./827-yongjoonseo.py)

