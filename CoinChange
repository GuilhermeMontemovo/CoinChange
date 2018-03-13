V = 10				# money
n = 2 				# number of different coins
coinValue = [1, 5]  # value of each coin


# Creates a list containing V+1 objects
memo = [-1 for x in range(V+1)] 


# recursion conditions:
# 1- change(0) = 0 -> is needed 0 coins to change 0 cents
# 2- change(< 0) = inf -> this change is too mmuch 
# 3- change(value) = 1 + min(change(value - coinValue[i])) for i in range(n-1)


def change(value):
	if memo[value] != -1:			# checking if alredy pass by this state 
		return memo[value]

	if value == 0: 					# recursion condition 1
		return 0

	if value < 0:					#recursion condition 2
		return float('inf')

	ans = float('inf')

	for i in range(n):			# recursion condition 3
		ans = min(1 + change(value - coinValue[i]), ans)

	memo[value] = ans
	return ans



print(change(V))