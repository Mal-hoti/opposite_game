# opposite_game
Code for the opposite game
 ```
 import random

list1=['Hot', 'Summer', 'Hard', 'Dry', 'Simple',
    'Light', 'Weak', 'Male', 'Sad', 'Win', 'Small',
    'Ignore', 'Buy', 'Succeed', 'Reject',
    'Prevent', 'Exclude']

list2=['Cold', 'Winter', 'Soft', 'Wet', 'Complex',
    'Darkness', 'Strong', 'Female', 'Happy',
    'Lose', 'Big', 'Pay attention', 'Sell', 'Fail',
    'Accept', 'Allow', 'Include']


print('Welcome to the opposite game.\nYour aim is to find the opposite of each word\nGood Luck!\n\n')
score = 0
def main():
    global score
    used = []
    wrong_ans = []
    duplicate = True
    for i in range(10):
        used.append(i)
        
        while duplicate:
            
            j = random.randint(0,len(list1)-1)
            if j not in used :
                
                
                duplicate = False
            elif i == j:
                duplicate =True
            else:
                
                duplicate = True
        
    


        print(i+1,') ',list1[i],'is to',list2[i],' as',list1[j],'is to ...\n:')
        user_input = input()
        
        used.append(j)
        if user_input.upper() == list2[j].upper():
            print("Correct!\n")
            score += 1
        else:
            print('Wrong\n')

            wrong_ans.append([list1[j],list2[j],i])
        duplicate = True


    print('Here are your mistakes:\n')
    for i in range(len(wrong_ans)):
        print((wrong_ans[i][2])+1,') ',(wrong_ans[i][1]).upper(),'is the opposite of',(wrong_ans[i][0]).upper())
main()
print('\n\nYour final score is: ',score)

play_again = input('\n\n\nType:\n1 to play again\n2 to quit')


            
                           



            
