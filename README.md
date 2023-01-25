# **ASSIGNMENT 1**

  Student ID :700749050
  
  Assignment by : Meghana Chodagiri
  
  Course: CS5710
  
  CRN Number: 232922
  
 Assignment Short Descrpition:
 
     Programs on Lists, Sets, Dictionaries, Tuples , String formatting, Strings , Mathematical programs using python language and Machine learning Algorithms like understanding K Nearest Neighbor algorithm, splitting of training and test data, analyzing the data model, computing the confusion matrix and calculating accuracy, sensitivity and specificity values.

Languages used:
          
    Python 3

Tools Used for the assignment :
        
    Jupyter Notebook
    Anaconda navigator
    Word Document
    Screen recording application
    Github
 
Installation process of anaconda and jupyter: 

     Go to the Anaconda Downloads page and download the 64-Bit Graphical Installer for Mac.

     Double click on the .pkg file and click Install.

     Read and agree to the licensing terms.

     Select if you want to install for ‘Just Me’ or ‘All Users’. If you are installing for ‘All Users’, you must have 4. Administrator privileges.

     You will be prompted to select the installation location. By default, Anaconda should try to install in your home directory. We recommend accepting        this default. Click Install.

     You will be asked if you want to add Anaconda to your PATH environment variable. Do not add Anaconda to the PATH because it can interfere with other        software.

    You will be asked if you want Anaconda to be your default version of Python. We recommend ‘Yes’. There are some rare instances where you would not make     Anaconda the default version, but they are beyond the scope of this article.

    Click the Install button.

    You may be asked if you want to install PyCharm. PyCharm is another IDE (similar to Jupyter Notebook) but is not necessary right now.

    Go ahead and finish the installation.

    Now you can verify your installation. Go to your Applications folder and double-click on Anaconda Navigator.

    Now we need to install a few key packages. In the BASH or zsh terminal, type:

    conda install jupyter

    Once the installation completes, in the BASH or zsh terminal, type:

    jupyter notebook

    A Jupyter Notebook interface will appear in your default browser.

    When prompted with ‘Proceed ([y]/n)?’ type y.


**Assignment Long description :**

Question 1

    The following is a list of 10 students ages:
    ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]
    • Sort the list and find the min and max age
    • Add the min age and the max age again to the list
    • Find the median age (one middle item or two middle items divided by two)
    • Find the average age (sum of all items divided by their number)
    • Find the range of the ages (max minus min)

Answer 1

    import statistics
    import math

    # Initializing the given list of 10 student ages
    ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]
    print(ages)

    Output: [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]

 # 1. Sort the list and find the min and max age

    # used default sort() method to sort and printing the list
    ages.sort()
    print("Sorted list is",ages)
    # using default max() and min () methods which are used to find max and min values in the list
    max_age = max(ages)
    min_age = min(ages)
    print("Max Age is", max_age)
    print("Min Age is", min_age)
 
Output :
Sorted list is [19, 19, 20, 22, 24, 24, 24, 25, 25, 26]
Max Age is 26
Min Age is 19

# 2. Add the min age and the max age again to the list

    # append() method is used to add items to the list by default, thereby adding min and max age  to the list
    ages.append(min_age)
    ages.append(max_age)
    print("List after adding min age and max age", ages)

 
Output :
List after adding min age and max age [19, 22, 19, 24, 20, 25, 26, 24, 25, 24, 19, 26]

# 3.Find the median age (one middle item or two middle items divided by two)
	# To find median of a list, first we need to sort the list
	# and calculate the median
	# importing math module to use floor function
	#sorting the list

	ages.sort()
	#finding the middle index
	middle_index= len(ages)/2
	# using math function floor to get the exact middle index
	exact_middle_index = math.floor(middle_index)
	# the median value will be the value of exact_middle_index
	median_value = ages[exact_middle_index]
	print("Median of ages is", median_value)

	# but here we can use also use inbuilt median method by importing Statistics module in py3
	print("Sorted list after adding min age and max age", ages)
	print("Median of ages is", statistics.median(ages))

 

Output:
Median of ages is 24
Sorted list after adding min age and max age [19, 19, 20, 22, 24, 24, 24, 25, 25, 26]
Median of ages is 24.0


# 4.Find the average age (sum of all items divided by their number)
	# To find average, we need to calculate the sum of all items in a list divided by number of items.
	# I have calculated sum and length of the list , assigned to a variage average and printed the average.
	list_sum = sum(ages)
	list_length = len(ages)
	average = list_sum/list_length
	print("Average of ages is ", average)

 
Output:
Average of ages is  22.8

# 5.Find the range of the ages (max minus min)

# subtracting the max value and min value of ages using (-) operator
range = max(ages) - min(ages)
print("Range of ages is ", range)

 

Output:
Range of ages is 7



Question 2

• Create an empty dictionary called dog
• Add name, color, breed, legs, age to the dog dictionary
• Create a student dictionary and add first_name, last_name, gender, age, marital status,
skills, country, city and address as keys for the dictionary
• Get the length of the student dictionary
• Get the value of skills and check the data type, it should be a list
• Modify the skills values by adding one or two skills
• Get the dictionary keys as a list
• Get the dictionary values as a list
Answer 2

#1.Create an empty dictionary called dog

	#created an empty dictionary dog
	dog = {}
	print(dog)


Output {}


# 2. Add name, color, breed, legs, age to the dog dictionary

	#dog = {'name':'Tommy'
	#       , 'color':'White',
	#       'breed':'husky',
	#       'legs':'short',
	#       'age': 3}

	# Adding keys and assigning values to the keys using assignment operator.
	dog["name"] = "Tommy"
	dog["color"] = "White"
	dog["breed"] = "Husky"
	dog["legs"] = "long"
	dog["age"] = 3
	print(dog)

	# We can also assign key-value pairs as follows
	dog = {'name':'Tommy'
	, 'color':'White',
	'breed':'Husky',
	'legs':'Long',
	'age': 3}

 
Output : {}
{'name': 'Tommy', 'color': 'White', 'breed': 'Husky', 'legs': 'long', 'age': 3}


# 3 Create a student dictionary and add first_name, last_name, gender, age, marital status,
#skills, country, city and address as keys for the dictionary

	# I have used imaginary data for key value pairs.
	student = {'first_name':'Meghana',
	'last_name':'Chodagiri',
	'gender':'Female',
	'age': 26,
	'marital_status': 'married',
	'skills' : ['python','java'],
	'country': 'India',
	'city':'Hyderabad',
	'address':'Hitech city'}
	print("Student Dictionary is " ,student)
 
Output : Student Dictionary is  {'first_name': 'Meghana', 'last_name': 'Chodagiri', 'gender': 'Female', 'age': 26, 'marital_status': 'married', 'skills': ['python', 'java'], 'country': 'India', 'city': 'Hyderabad', 'address': 'Hitech city'}

# 4. Get the length of the student dictionary


	# Printing lenth of the dictionary using in-built len() method
	print("The length of student dictionary is",len(student))


Output : The length of student dictionary is 9


# 5. Get the value of skills and check the data type, it should be a list

	#Getting value of skills using get() method, which will get the value of key as shown below
	print(student.get('skills'))

	# printing data type of skills, where type() method will return the type of the key.
	print(type(student['skills']))

 
Output: ['python', 'java']
<class 'list'>


# 6. Modify the skills values by adding one or two skills

	# Getting list in dict and adding extra skills to the list
	# I have called the value of the skills and appending a extra data at the end to skills list
	student['skills'] = student.get('skills', []) + ['R','C#']
	print(student)

 

Output: dictionary after updating lst is {'first_name': 'Meghana', 'last_name': 'Chodagiri', 'gender': 'Female', 'age': 26, 'marital_status': 'married', 'skills': ['python', 'java', 'R', 'C#'], 'country': 'India', 'city': 'Hyderabad', 'address': 'Hitech city'}


# 7. Get the dictionary keys as a list

	# for getting only keys , we use list.keys() method and changing it to the list using list() method ans assigning to another list
	keysList = list(student.keys())
	print(keysList)


# 8• Get the dictionary values as a list

	# for getting only values , we use list.values() method and changing it to the list using list() method and assigning to another list.
	valuesList = list(student.values())
	print(valuesList)



Output:
dictionary after updating lst is {'first_name': 'Meghana', 'last_name': 'Chodagiri', 'gender': 'Female', 'age': 26, 'marital_status': 'married', 'skills': ['python', 'java', 'R', 'C#'], 'country': 'India', 'city': 'Hyderabad', 'address': 'Hitech city'}

List of keys is ['first_name', 'last_name', 'gender', 'age', 'marital_status', 'skills', 'country', 'city', 'address']

Values of keys is  ['Meghana', 'Chodagiri', 'Female', 26, 'married', ['python', 'java', 'R', 'C#'], 'India', 'Hyderabad', 'Hitech city']


Question 3
• Create a tuple containing names of your sisters and your brothers (imaginary siblings are
fine)
• Join brothers and sisters tuples and assign it to siblings
• How many siblings do you have?
• Modify the siblings tuple and add the name of your father and mother and assign it to
family_members

Answer 3:


# 1.• Create a tuple containing names of your sisters and your brothers (imaginary siblings are
# fine)
	# created a tuple using () and adding brothers and sisters to it.
	brothers =("Jyothsna","Dheeru","Sai")
	print("Brothers tuple is", brothers)


Output: Brothers tuple is ('Jyothsna', 'Dheeru', 'Sai')

#2. 	
	
	sisters = ("Ammu","Madhavi")
	Join brothers and sisters tuples and assign it to siblings
	siblings = brothers + sisters
	print("My siblings are", siblings)

Output is :
Brothers tuple is ('Jyothsna', 'Dheeru', 'Sai')
My siblings are ('Jyothsna', 'Dheeru', 'Sai', 'Ammu', 'Madhavi')


#3. How many siblings do you have?

	print("I have", len(siblings), "siblings")

#4. Modify the siblings tuple and add the name of your father and mother and assign it to
#family_members

	# converting into list

	x= list(siblings)

	# appending members to the tuple
	x.append('Sudha')
	x.append('Srinu')
	family_members = tuple(x)
	print("My family members are" ,family_members)


 

Output:
I have 5 siblings
My family members are ('Jyothsna', 'Dheeru', 'Sai', 'Ammu', 'Madhavi', 'Sudha', 'Srinu')

Question 4:


it_companies = {'Facebook', 'Google', 'Microsoft', 'Apple', 'IBM', 'Oracle', 'Amazon'}
A = {19, 22, 24, 20, 25, 26}
B = {19, 22, 20, 25, 26, 24, 28, 27}
age = [22, 19, 24, 25, 26, 24, 25, 24]
• Find the length of the set it_companies
• Add 'Twitter' to it_companies
• Insert multiple IT companies at once to the set it_companies
• Remove one of the companies from the set it_companies
• What is the difference between remove and discard
• Join A and B
• Find A intersection B
• Is A subset of B
• Are A and B disjoint sets
• Join A with B and B with A
• What is the symmetric difference between A and B
• Delete the sets completely
• Convert the ages to a set and compare the length of the list and the set.

Answer4:

	it_companies = {'Facebook', 'Google', 'Microsoft', 'Apple', 'IBM', 'Oracle', 'Amazon'}
	A = {19, 22, 24, 20, 25, 26}
	B = {19, 22, 20, 25, 26, 24, 28, 27}


	#Find the length of the set it_companies.
	#I have used len() method to get length of set
	print("length of the set it_companies", len(it_companies))



#• Add 'Twitter' to it_companies
	#Using add() method to add an item to set
	it_companies.add("Twitter")
	print(it_companies)

 
Output: {'Facebook', 'Google', 'Twitter', 'IBM', 'Amazon', 'Apple', 'Oracle', 'Microsoft'}


	#• Insert multiple IT companies at once to the set it_companies
	# I have used another set multi_it to add items at once and updated the existing set
	multi_it = {'Walmart','Tesla', 'TCS','Infosys', 'Accenture'}
	it_companies.update(multi_it)
	print(it_companies)

 

Output: {'TCS', 'Tesla', 'Google', 'Walmart', 'Twitter', 'Accenture', 'Apple', 'Microsoft', 'Facebook', 'IBM', 'Amazon', 'Infosys', 'Oracle'}

#• Remove one of the companies from the set it_companies
	#using remove() method to delete an item.
	it_companies.remove('Infosys')
	print(it_companies)



Output: {'TCS', 'Tesla', 'Google', 'Walmart', 'Twitter', 'Accenture', 'Apple', 'Microsoft', 'Facebook', 'IBM', 'Amazon', 'Oracle'}


What is the difference between remove and discard

	Both remove() and discard() we delete items from set, but if the item to remove
	does not exist in the set, discard() will NOT raise an error.

	#it_companies.remove('Dell')
	#print(it_companies)
	it_companies.discard('Dell')
	print(it_companies)
 



#• Join A and B

	# Using union() method to join both sets.
	c = A.union(B)
	print(c)

 
Output: {19, 20, 22, 24, 25, 26, 27, 28}


#• Find A intersection B

	# using intersection() to get the unique items in 2 sets.
	t = A.intersection(B)
	print("A intersection B is",t)


Output: A intersection B is {19, 20, 22, 24, 25, 26}

#• Is A subset of B

	# using issubset() method to find if A is subset of B
	sub = A.issubset(B)
	print("Is A subset of B" ,sub)


#• Are A and B disjoint sets

	disjoint = A.isdisjoint(B)
	print("Is A disjoint of B",disjoint)



Output:
Is A subset of B True
Is A disjoint of B False

#• Join A with B and B with A

	#Joining A and B  and assingning to c, Joining B and C and assigning to d,
	# joining c and d using union()
	c = A.union(B)
	d = B.union(A)
	e = c.union(d)
	print("Join A with B and B with A",e)

#• What is the symmetric difference between A and B

	#Return a set that contains all items from both sets, except items that are present in both sets:
	#using symmetric_difference() to find the items that are not present in another set.
	symm = A.symmetric_difference(B)
	print("items that are not present in A are", symm)


Output: Join A with B and B with A {19, 20, 22, 24, 25, 26, 27, 28}
items that are not present in A are {27, 28}

#• Delete the sets completely

	# Clear() will delete the sets completeley and returns set()
	it_companies.clear()
	A.clear()
	B.clear()
	print(it_companies)
	print(A)
	print(B)


Output:
set()
set()
set()


#• Convert the ages to a set and compare the length of the list and the set.

	age = [22, 19, 24, 25, 26, 24, 25, 24]
	#converting the list to set using set()
	age_set = set(age)
	print(age_set)
	# list can have duplicate items, but the set cannot have duplicate items, os the length varies.
	print("the length of list is" ,len(age), "and the length of set is" ,len(age_set))

 

Output:

{19, 22, 24, 25, 26}
the length of list is 8 and the length of set is 5



Question 5
The radius of a circle is 30 meters.
• Calculate the area of a circle and assign the value to a variable name of _area_of_circle_
• Calculate the circumference of a circle and assign the value to a variable name of
_circum_of_circle_
• Take radius as user input and calculate the area.

Answer 5:
# Question 5
#The radius of a circle is 30 meters.

	r = 30

	#• Calculate the area of a circle and assign the value to a variable name of _area_of_circle_
	# taking pi as 3.14
	pi= 3.14

	#using area of circle as pi *r *r
	_area_of_circle_ = pi * r * r
	print("The area of circle is", _area_of_circle_)


	#• Calculate the circumference of a circle and assign the value to a variable name of
	#_circum_of_circle_

	# the circumference of circle is 2 * pi * r

	_circum_of_circle_ = 2 * pi * r
	print("The circumference of circle is", _circum_of_circle_)

 
Output:
The area of circle is 2826.0
The circumference of circle is 188.4

#• Take radius as user input and calculate the area.

	r = float(input('Enter the radius of the circle :'))
	_area_of_circle_ = pi * r * r

	print(f"Area of the circle is : %.2f" % _area_of_circle_)

 
 
Output:
Enter the radius of the circle :30
Area of the circle is : 2826.0

Question 6:

“I am a teacher and I love to inspire and teach people” • How many unique words have been used in the sentence? Use the split methods and set to get the unique words.

Answer 6:


	str = "I am a teacher and I love to inspire and teach people"

	#How many unique words have been used in the sentence? Use the split methods and set
	#to get the unique words.

	# I have used split() method to split the given string into words .
	# I am converting the string using set() as set doesn’t have unique words
	unique_words = set(str.split())
	print(unique_words)

	#using len() to get the len of the set.
	length = len(unique_words)
	print("number of unique words set is",length)

 
Output:
{'I', 'people', 'to', 'teacher', 'teach', 'a', 'am', 'and', 'inspire', 'love'}
number of unique words set is 10

Question 7:
Use a tab escape sequence to get the following lines.
Name Age Country City
Asabeneh 250 Finland Helsinki

Answer 7:

	# Tab escape sequence is used for string formatting and giving a tab space between words or numbers.

	print("Name\tAge\tCountry\tCity\nAsabeneh250\tFinland\tHelsinki")
 
Output:
Name	Age	Country	City
Asabeneh250	Finland	Helsinki

Question 8:
Use the string formatting method to display the following:
radius = 10
area = 3.14 * radius ** 2
“The area of a circle with radius 10 is 314 meters square.”

Answer 8:

	#Use the string formatting method to display the following:
	#radius = 10
	#area = 3.14 * radius ** 2
	#“The area of a circle with radius 10 is 314 meters square.”
	radius = 10

	# we use string formatting if we need to insert the value of an object, variable, or expression into another string.
	print(f"The area of a circle with radius {radius} is {round(3.14 * radius**2)} meters square.")


 

Output: The area of a circle with radius 10 is 314 meters square.



Question 9
Write a program, which reads weights (lbs.) of N students into a list and convert these weights to
kilograms in a separate list using Loop. N: No of students (Read input from user)
Ex: L1: [150, 155, 145, 148]
Output: [68.03, 70.3, 65.77, 67.13]

Answer 9:

	#taking an empty list for lists of students weights in pounds and kgs
	L1 = []
	kgs_lst = []
	# number of students as input
	N = int(input("Enter number of students : "))

	# iterating till the range N, where N is number of students.
	for i in range(0, N):
	ex = int(input())
	L1.append(ex)  # adding the weight one by one
	kgs = ex/2.2046    # converting pounds to kgs by dividing pound weight with 2.2046
	kgs_lst.append(round(kgs,2)) # rounding up to 2 decimals
	print("List of weights in pounds",L1)
	print("List of weights in kgs",kgs_lst)

 

Output:
Enter number of students : 4
150
155
145
148
List of weights in pounds [150, 155, 145, 148]
List of weights in kgs [68.04, 70.31, 65.77, 67.13]


Question 10.

Question 10
The diagram below shows a dataset with 2 classes and 8 data points, each with only one feature
value, labeled f. Note that there are two data points with the same feature value of 6. These are
shown as two x’s one above the other. Provide stepwise mathematical solution, do not write
code for it.

 
1. Divide this data equally into two parts. Use first part as training and second part as
testing. Using KNN classifier, for K=3, what would be the predicted outputs for the test
samples? Show how you arrived at your answer.
2. Compute the confusion matrix for this and calculate accuracy, sensitivity and specificity
values.

Answer

	Given:

	Total classes = 2, Considering the two classes as class A and Class B
	Data points =8
	Feature = 1 f
	K=3

	Explanation for the predicted outputs for test samples:

	Step 1: K= 3 which means, considering the test sample has 3 nearest neighbors.
	We have 2 datapoints on same feature value.
	Step 2:   Dividing the dataset into Training data and test data.

	Given Training data is TR = 1,2,3,4,5,6,7,8,9,10,11,12,13
	And I have considered Test Samples as TS = 1, 3, 5, 7, 9, 11
	Consider, Class A is
	Class B is
	According to the data model, the training data is classified as below.

	Training Data (TD)
	Input	Target (Class)
	1	A
	2	A
	3	B
	6	B
	6	B
	7	A
	10	A
	11	A





	According to the training data, the test data samples, outputs can be predicted as below.

	For TS=1, Neighbors are TD=1, TD=2, TD=3-> Output Class = A
	For TS=3, Neighbors are TD=2, TD=3, TD=4, -> Output Class = B
	For TS=5, Neighbors are TD=4, TD=5, TD=6, TD = -> Output Class = B
	For TS=7, Neighbors are TD=7, TD=8 -> Output Class = B
	For TS=9, Neighbors are TD=9, TD=10 -> Output Class = A
	For TS=11, Neighbors are TD=12, TD=13 -> Output Class = A
	So, the below table will be the outputs of test data.

	Test Data Input	Predicted output class
	1	A
	3	B
	5	B
	7	B
	9	A
	11	A



	Finally, the predicted outputs of test data samples can be both A and B class.


	2. We can calculate confusion matrix by comparing predicted outputs with actual output using below formula.

	Based on above values we can compute Confusion Matrix as -

	True Positives (TP) = 1(Output of 3 in Test Set is B & Predicted Output by KNN is also B)
	True Negatives (TN)= 0 (Output of 1 in Test Set is A & Predicted Output by KNN is also A) False Positives (FP) = 0 (Output of 7in Test Set is A & Predicted Output by KNN is B) False Negatives (FN)= 1 (Output in Test Set is B & Predicted Output by KNN is A)
	Confusion Matrix: Confusion Matrix is the matrix as output and describes the complete performance of the model.
		A (0)	B (1)
	0	0(TN)	0(FN)
	1	0(FP)	1(TP)
	Accuracy Rate = (Number of Correct Predictions / Total Number of Predictions) × 100%
	= (TP+TN/P+N) ×100%
	= (1+01+0+0+1+1)/8 ×100%
	=50%

	Sensitivity or True Positive Rate or Recall Rate: True Positive Rate is defined as TP/ (FN+TP). True Positive Rate corresponds to the proportion of positive data points that are correctly considered as positive, with respect to all positive data points.
	 =TP/TP+FN
	=1/1+1
	=1/2
	=50%

	Specificity or True Negative Rate: True Negative Rate is defined as TN / (FP+TN). False Positive Rate corresponds to the proportion of negative data points that are correctly considered as negative, with respect to all negative data points.

	=(TN/TN+FP) x100
	= (0/0+0)×100
	=Undefined












