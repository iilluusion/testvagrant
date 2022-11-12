Problem 1 -> Create a small data structure that holds details - Name of the team, points they have earned and result of last 5 matches as per above image.

Sol 1 ->

I used a class name "TEAM" for teams in data.

Implemented four methods and three attributes.

i) add_team(self,team,points,last5) --> creates an object of class team and append the object in the list(global variable) ipl, as an object got created constructor gets called and all attributes gets intiliazed.

ii) show_data(self) --> prints all attributes of object of class team (using format to show data in tabular way)

iii) get_points(self) --> return the value of attribute points

iv) get_last5(self) --> return the value of attribute last 5 matches results

v)name --> name of team

vi)points --> points obtained by a team

vii)last5 --> record of last five matches

Then in main function adds all the teams data to object i which actually appends it to ipl list.

Problem 2 -> Programmatically retrieve the teams that have 2 consecutive losses.

Sol 2 ->

Implemented a function named cons_loss which is actually a generalise function for n consecutive win/loss.

cons_loss(loss,result) --> i) here loss is the number of loss/win and result is whether it is win or loss("W" for win/"L" for loss)

 			   ii) I have declared a empty list as res which I'll later use to add the teams which got filtered.

 			   iii) Runs a loop to the range of ipl list so it will number 10 times because we added ten 
 				  objects in ipl list.

 			   iv) Then we retrieve last5 match records using method get_last5 and storing it in a string s

 			   v) Intiliaze two integers as count and conloss, count will keep the count of current number of 
 				consecutive loss/win and conloss will keep the maximum count of consecutive loss or wins.

 			   vi) Runs another loop as range is length of string s which we got in step iv

 			   vii) Compares if current match(s[i]) is as the result(step i) we increases count by 1 
 				  then assign the max value between conloss and count to conloss.

 			   viii) If result is not equal to current match then make count zero because we want consecutive matches 

 			   ix) when the second loop ends it compares if consloss is equal to loss then add the object to res list.

 			   x) Return res as output.
For this Case of two consecutive loss the value of: loss = 2 result = "L"

i) First we call the function cons_loss(2,"L") and assign it res.

ii) It return a list where various team get filtered.

iii) We caluclates the sum of points of all these filtered teams and divides them by the number of filtered teams, That's how we get our avg. points.

Problem 3 -> Generalize the same solution, so that we could get teams that have n consecutive losses/wins.

Solution 3 ->

Already explained about the function in solution 2
Problem 4 -> Once the above is done, Calculate the average points of these filtered teams

Solution 4 ->

Implements a function as queries(which in genreal refers to queries)

 queries() -> i) Ask for a integer as input if want to see:
 		Press 1 for points table.
 		Press 2 to search consecutive win/loss teams
 		Press any other digit to exit.

 		ii) Used exception handling to get only valid input for this

 		iii) if n==1 all the data of the teams will be displayed.

 		iv) if n==2 it'll take the input of num(taken as loss in function) and result for the con_loss function

 		v) It'll give us our filtered teams in res list 

 		vi)Then we will display all the filtered teams and after that calc. all the sum of points.

 		vii)Then we will check if length of res list is not zero(because it'll give zero division error)
 		    it'll display the avg. points of filtered teams.

 		viii) If length is zerp it'll not display anything and queries function will be called.