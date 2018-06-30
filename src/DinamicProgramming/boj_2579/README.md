 * dp문제를 풀기 위해서 점화식을 찾아야한다.
 * 
 * topdown방식으로 점화식을 구하는 과정. 
 * N번째를 파악하기 위해, 그 다음 단계가 어떤 형태일지, 
 * 또는 그 전 단계가 어떤 형태일지 파악하면서 구한다.
 * 
 * 여기선 그 전 단계를 파악하면서 점화식을 구해본다. 
 * dp[N]번째를 구하고 싶을때, 다음과 같은 세가지 경우가 있다 
 * 1. dp[N][0] 안밟는 경우
 * 2. dp[N][1] 계단을 1회째 밟은 경우
 * 3. dp[N][2] 계단을 2회째 밟은 경우
 * 
 * 그리고 N단계에 오기 직전 단계가 어땠을지 생각하면 된다.
 * 1.의 경우에, N에서 안밟으려면, N-1에선 꼭 밟아야한다.
 * 그러므로 dp[N-1][1], dp[N-1][2] 둘 중 큰 값을 가진 경로를 
 * 지나왔다고 생각하고 dp[N][0]에 값을 입력하면 된다.
 * 2.의 경우에는, N에서 1회 밟으려면 N-1에서는 0회를 밟았어야 한다.
 * 3.의 경우에는 N에서 2회를 밟으려면, N-1에서는 1회를 밟았어야 한다.
 * 
 * 이제 N단계를 구하기위한 모든 경우의 점화식이 완성되었다.
 * 구현을 해보자