- [CountDiv](https:app.codility.com/programmers/lessons/5-prefix_sums/count_div/)

## ���� ���
# ù�� ° ���
	1. end�� start���̿� k�� ��� ������ ������
	2. �׸��� start��  end��  k�� ������ �������ٸ� +1�� ������.

# �ι� ° ���
	1. 0����  end���� k�� ���� ���� �� �� �ִ��� ������
	2. 0����  start���� k�� �������� �� �� �ִ��� ������
	3. start�� k�� ����϶��� +1�� �߰��Ѵ�, ���� : ���� ���ð� start�� ������ �������� ���ϱ⸦ �����ϱ� ����
	4. (1)-(2)�� ������

## �ҽ��ڵ�

~~~java
public int solution(int A, int B, int K) {
	
	return this.test(A, B, K);
}
public int test(int start, int end, int k){
	int temp = end/k - start/k;
	if(temp%k==0){
		temp+=1;
	}
	return temp;
}
~~~

## ��������

## �ð����⵵�� �ָ��� ���� ������ ��, �ݿ��� ��

## ä�� ���
| Task Score | Correctness | Performance | 
| ------------ | ------------- | ------------- |
| 100% | 100% | 100% |
