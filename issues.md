# Issues
## Hovering Setup
 * 이슈 : takeoff 시 soaring 이슈
   * 기체
     * 450 frame
     * 기체번호 : x
   * 증상
     * arming 이후 throttle을 조금 올리는 경우 갑자기 솟아 오르는 현상
   * 시도
     * 완전 초기화 이후에도 동일 현상 발생
     * 다른 2개 비행체 시료에서 동일 설정 후 비행시 문제 없음
     * PX4를 올려서 테스트 시 문제 없음 -> FC 자체 문제는 아닌 것으로 보임
   * Log
     * [링크](logs/190305_soaring.bin)
 * 이슈 : 배터리 4S vs. 3S
   * 기체 
     * 450 frame
   * 증상
     * 4S의 경우 throttle을 조금만 줘도 Output이 커져서 soaring 되는 현상 발견
     * 3S와 비교했을 thrust가 강함
   * 시도
     * throttle max 값을 조정 -> 2000에서 1700으로 조정. trim도 1350으로 조정 (1600으로 조정시 값이 낮다고 arming이 안됨)
