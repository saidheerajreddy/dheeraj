## Lab: 31-12-2019

1. Take values of length and breadth of a rectangle from user and check if it is square or not.
	```
		l = int(input("Enter Length: "))
		b = int(input("Enter Breadth: "))

		if l == b:
			print("It's a square")
		else:
			print("It's a rectangle")	
	```

2. Take two int values from user and print greatest among them.
	```
		a = int(input("Enter a number: "))
		b = int(input("Enter a number: "))

		if a > b:
			print(f"{a} is greater than {b}")
		elif b > a:
			print(f"{b} is greater than {a}")
		else:
			print(f"{a} is equal to {b}")
	```

3. A shop will give discount of 10% if the cost of purchased quantity is more than 1000. Ask user for quantity. Suppose, one unit will cost 100. Judge and print total cost for user.
	```
		q = int(input("Enter quantity: "))
		t = 100 * q

		if t > 1000:
			t *= 0.9

		print(f"Total cost for {q} items: {t}")
	```

4. A company decided to give bonus of 5% to employee if his/her year of service is more than 5 years. Ask user for their salary and year of service and print the net bonus amount.
	```
		sal = float(input("Enter salary: "))
		yrs = int(input("Enter Years of Service: "))

		bonus = 0
		if yrs > 5:
			bonus = 0.05 * sal

		print(f"Salary: {sal}")
		print(f"Bonus: {bonus}")
		print(f"Total: {sal+bonus}")
	```

5. A school has following rules for grading system:
  * Below 25 - F
	* 25 to 45 - E
	* 45 to 50 - D
	* 50 to 60 - C
	* 60 to 80 - B
	* Above 80 - A <br>
	Ask user to enter marks and print the corresponding grade.

	```
		marks = float(input("Enter Marks: "))

		if marks >= 80:
			grade = 'A'
		elif marks < 80 and marks >= 60:
			grade = 'B'
		elif marks < 60 and marks >= 50:
			grade = 'C'
		elif marks < 50 and marks >= 45:
			grade = 'D'
		elif marks < 45 and marks >= 25:
			grade = 'E'
		else:
			grade = 'F'

		print(f"Marks: {marks}\nGrade: {grade}")
	```

6. Take input of age of 3 people by user and determine oldest and youngest among them.
	```
		print("Enter Ages:")
		ages = [int(input()), int(input()), int(input())]
		print(f"Youngest: {min(ages)}\nOldest: {max(ages)}")
	```

7. A student will not be allowed to sit in exam if his/her attendence is less than 75%. <br>
	Take following input from user
	* Number of classes held
	* Number of classes attended. <br>
	And print percentage of class attended and if student is allowed to sit in exam or not.
	```
		held = int(input("Enter Number of classes held: "))
		att = int(input("Enter Number of classes attended: "))

		per = att / held * 100

		print(f"Attendence: {per:.2f}%")
		print("Allowed to write Exam" if per >= 75 else "Not allowed to write Exam")
	```

8. Modify the above question to allow student to sit if he/she has medical cause. Ask user if he/she has medical cause or not ( 'Y' or 'N' ) and print accordingly.
	```
		held = int(input("Enter Number of classes held: "))
		att = int(input("Enter Number of classes attended: "))
		mc = input("Do you have a medical cause (Y/N): ")

		per = att / held * 100

		print(f"Attendence: {per:.2f}%")
		print("Allowed to write Exam" if per >= 75 or mc.lower() == 'y' else "Not allowed to write Exam")
	```

9. Write a python program to create a list of first 10 natural numbers.
	```
		nos = [i for i in range(1, 11)]
		print(nos)
	```
	
10. Write a python program to create a list of first 10 natural numbers in reverse order.
	```
		nos = [i for i in range(10, 0, -1)]
		print(nos)
	```

11. Write a python program to create a list of even numbers which are less than 20.
	```
		nos = [i for i in range(0, 20, 2)]
		nos = [i for i in range(0, 20) if i % 2 == 0] # Another way
		print(nos)
	```

12. Write a python program to create a list of odd numbers which are less than 20 in reverse order.
	```
		nos = [i for i in range(19, 0, -2)]
		nos = [i for i in range(19, 0, -1) if i % 2 != 0] # Another way
		print(nos)
	```

13. Write a python program to create a list from a given string and word.
	```
		s = input("Enter a string: ")
		l = list(s)
		print(l)
	```

14. Write a python program to create a list from a given number.
	```
		n = int(input("Enter Range: "))
		arr = [i for i in range(1,n+1)]
		print(arr)
	```

15. Write a python program to create an empty list and add the elements by reading from the user.
	```
		arr = []

		print("Enter numbers: (End by entering a character)")
		while True:    
			try:
				ele = int(input())
				arr.append(ele)
			except ValueError:
				break

		print(f"Array: {arr}")
	```

16. Write a python program to print 'g' from the following list [2,5,'a',6,[9,'g',7]]
	```
		arr = [2,5,'a',6,[9,'g',7]]
		print(arr[4][1])
		print(arr[-1][1])
		print(arr[4][-2])
		print(arr[-1][-2])
	```

17. Write a python program to add an element in above list at 4th position.
	```
		arr = [2,5,'a',6,[9,'g',7]]
		ele = input("Enter an element: ")
		arr.insert(4, ele)
		print(arr)
	```

18. Write a python program to get the index of 6 in above list.
	```
		arr = [2,5,'a',6,[9,'g',7]]
		print(arr.index(6))
	```

19. Write a python program to join 2 different lists.
	```
		list1 = ['a', 'b', 'c']
		list2 = [1, 2, 3]
		print(f"1st List Before: {list1}")
		print(f"2nd List Before: {list2}")

		list1.extend(list2)

		print(f"1st List After: {list1}")
		print(f"2nd List After: {list2}")
	```

20. Write a python program to sort a list in ascending and descending order.
	```
		l = list(map(int, input("Enter Elements seperated by ',': ").split(',')))
		print(f"List: {l}")

		l.sort()
		print(f"Ascending Order: {l}")
		l.sort(reverse=True)
		print(f"Decending Order: {l}")
		
		# Another way
		print(f"Ascending Order: {sorted(l)}")
		print(f"Decending Order: {sorted(l, reverse=True)}")
	```

21. Write a python program to find maximum and minimum number in a list.
	```
		l = list(map(int, input("Enter Elements seperated by ',': ").split(',')))
		print(f"Minimum: {min(l)}")
		print(f"Maximum: {max(l)}")
	```

22. Write a python program to find how many times the number 2 has occurred in the following list [1,2,3,'a',2,7,9,2]
	```
		arr = [1,2,3,'a',2,7,9,2]
		print(arr.count(2))
	```

23. Write a python program to delete all elements from the list.
	```
		arr=[1,2,3,'a',2,7,9,2]

		print(f"Before: {arr}")
		for _ in range(len(arr)):
			arr.pop()
		print(f"After: {arr}")

		# Another way
		print(f"Before: {arr}")
		for _ in range(len(arr)):
			del arr[0]
		print(f"After: {arr}")

		# Another way
		print(f"Before: {arr}")
		arr = []
		print(f"After: {arr}")
	```

24. Write a python program to find whether a given element is present in the list or not.
	```
		arr = list(map(int, input("Enter Elements seperated by ',': ").split(',')))
		ele = int(input("Enter element to find: "))

		if ele in arr:
			print(f"{ele} is present in {arr}")
		else:
			print(f"{ele} is not present in {arr}")
	```

25. Given a list of numbers, write a python program which returns True if first and last number of a list is same.
	```
		arr = list(map(int, input("Enter Elements seperated by ',': ").split(',')))

		if arr[0] == arr[-1]:
			print(f"First and Last number of a list are same.")
		else:
			print(f"First and Last number of a list are not same.")
	```

26. Given a two list of numbers write a python program to create a third list such that it should contain only odd numbers.
	```
		l1 = list(map(int, input("Enter Elements seperated by ',': ").split(',')))
		l2 = list(map(int, input("Enter Elements seperated by ',': ").split(',')))
		l3 = []

		l3.extend([i for i in l1 if i % 2 != 0])
		l3.extend([i for i in l2 if i % 2 != 0])
		print(l3)
	```

27. Write a Python program to remove duplicates from a list.
	```
		l1 = list(map(int, input("Enter Elements seperated by ',': ").split(',')))
		
		l2 = list(set(l1))
		print(l2)

		# Another Way
		l2 = list(dict.fromkeys(l1))
		print(l2)
	```

28. Take 10 integers from keyboard using loop and print their average value on the screen.
	```
		arr = []
		print("Enter 10 Numbers: ")

		for _ in range(10):
 			arr.append(int(input()))

		avg = sum(arr)/len(arr)
		print("Average:", avg)
	```

29. Print all elements of a list using for loop.
	```
		arr=[1,2,3,'a',2,7,9,2]

		for ele in arr:
 			print(ele)
	```
