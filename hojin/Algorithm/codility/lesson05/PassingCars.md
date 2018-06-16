- [PassingCars](https://app.codility.com/programmers/lessons/5-prefix_sums/passing_cars/)

## ���� ���
# ù�� ° ���
	1. �Է� �迭�� �� ���� 0�� �ε����� ������ ����Ǵ� �迭�� ����� int zero[]
	2. �Է� �迭�� �� ���� 1�� �ε����� ������ ����Ǵ� �迭�� ����� int one[]
	3. �̽�����
		1. (P,Q)�� ������ ������ �� P < Q��� ������ �ִ�
		2. �̸� �ذ��ϱ� ���ؼ� (1),(2)�� �۾���
		3. if(zero[i] > one[j]) �� ��� Ž���� �����ϰ� i++�� ���� �� (�ݺ���). ( �� �迭�� ���� �Է� �迭�� �ε����� �����ϰ� �ִ�. )
		

# �ι� ° ���
 ù��° ����� 2�� for���� ���� ������ ������ �ʿ���
 `P < Q �ذ��ϱ�`
 1. �� ���� ������ (P,Q)�� ���Ѵ�
	1. P�� ���� 0�� �Է� �迭�� �ε���
	2. Q�� ���� 0�� �Է� �迭�� �ε���
 2. Q�� ������ n���� ���Ѵ�.
	1. ���� P�� �ε������� ���� Q���� �� ���� �ȴ�. ( P < Q ���� ���� ) --> n = n-1
		
## �ҽ��ڵ�

~~~java
	public int solution(int[] A) {
        // write your code in Java SE 8
		return this.test(A);
	}
	
	public int test(int[] a){
		int zeroCnt = 0;
		int oneCnt = 0;
		int total = 0;
		for(int i=0; i<a.length;i++){
			if(a[i]==0){
				zeroCnt++;
			}else{
				oneCnt++;
			}
		}
		for(int i=0;i<a.length;i++){
			if(total >1000000000){
				return -1;
			}
			if(a[i]==0){
				total += oneCnt;
			}else{
				oneCnt--;
			}
		}
//		System.out.println(total);
		return total;
	}
~~~

## ��������

## �ð����⵵�� �ָ��� ���� ������ ��, �ݿ��� ��

## ä�� ���
| Task Score | Correctness | Performance | 
| ------------ | ------------- | ------------- |
| 100% | 100% | 100% |