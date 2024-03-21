# Counting-digits-in-base
Raj loves to play with numbers. He has an integer N. Find the number of digits that N has in base K. Input The input contains two space-separated integers in the following format: N K  Constraints All values in the input are integers. 1 ≤ N ≤ 109 2 ≤ K ≤ 10

def count_digits_in_base(N, K):
    # Convert N to base K
    base_K_representation = ''
    while N > 0:
        remainder = N % K
        base_K_representation = str(remainder) + base_K_representation
        N //= K

    num_digits = len(base_K_representation)
    return num_digits

N, K = map(int, input().split())

result = count_digits_in_base(N, K)
print(result)
