---
jupytext:
    formats: md:myst
    text_representation:
        extension: .md
        format_name: myst
rise:
    start_slideshow_at: beginning

kernelspec:
    display_name: Python 3
    language: python3
    name: python3
---



# 部分优秀作业(PS7) #

## Quiz ##

### 张奕瑶 ###

```{code-cell} python3

def QUIZ():
    print ("Quiz time!")
    x=0
    a=int(input("How many books are there in the Harry Potter series? "))
    if a==7:
        print ("Correct")
        x=x+1
    else:
        print ("No")
    e=int(input("What is the famous book in the Ender series? 1.Ender's Game 2.Ender's Shadow 3.Speaker for the Dead 4.Xenocide "))
    if e==1:
        print ("Correct")
        x=x+1
    else:
        print ("No")
    b=float(input("What is 3*2.3?"))
    if str(b)=="6.9":
        print ("Correct")
        x=x+1
    else:
        print ("No")
    c=str(input("近代原子论是由谁提出的？A. 道尔顿B. 汤姆生C. 卢瑟福"))
    if c=="A":
        print ("Correct")
        x=x+1
    else:
        print ("No")
    d=int(input("Who is on the front of a one dollar bill?1. George Washington2. Abraham Lincoln3. John Adams4. Thomas Jefferson"))
    if d==2:
        print ("Correct")
        x=x+1
    else:
        print ("No")
    print("Congratulations, you got "+str(x)+" answers right.")
    print("That is a score of "+str(x/5*100)+" percent.")
QUIZ()

```

### 朱镜轩 ###
```{code-cell} python3

def quiz():
count = 0
print("Electronic devices are not allowed, please make sure your academic integrety.")
print("WHo is the most handsome person in scls?")
a =input("Type the answer here:")
if(not a =="Wilson"):
print("Correct!")
count = count +1
else:
print("No")

    print("Who benefits the Song Dynasty best?")
    print("A.WangAnShi")
    print("B.QingHui")
    print("C.Mr.Travess")
    print("D.Su Shi")
    b =input("Type the answer here:")
    if( b =="D"):
        print("Correct!")
        count =count+1
    elif( b =="A"):
        print("In my opinion, I don't think so.")
        count = count+0.5
    elif( b =="C"):
        print("I know, but i can't give you this credit.")
    else:
        print("No")
    
    print("Which of the following will cause the decrease of economic mobility?")
    print("A.Inflation")
    print("B.Deflation")
    print("C.The decrease of bank rate")
    print("D.The import of APCS teaching materials")
    c =input("Type the answer here:")
    if( c =="B"):
        print("Correct!")
        count =count +1
    elif( c =="D"):
        print("Seriously?")
    else:
        print("No")
        
    print("Which of the following scientist studies in order to revenge to his classmate?")
    print("A.Isaac Newton")
    print("B.ChenYiXin")
    print("C.Albert Einstein")
    print("D.David Ricardo")
    d =input("Type the answer here:")
    if( d =="A"):
        print("Correct!")
        count =count+1
    elif( b =="B"):
        print("Perhaps,i don't know.")
    else:
        print("No")
        
    print("The value of 1/2+1/4+1/8+...+1/n is infinite or not? (Yes or No)")
    e =input("Type the answer here:")
    if(e =="No"):
        print("Correct!")
        count= count+1
    else:
        print("No")
        
    print("A man is pushing a box of 6.67kg in an angle of 34.7 above the ground, set the coefficient of frictional force is 0.12. Please derive the work done by net force in this constant motion.")
    f = int(input("Type the answer here:"))
    if(f == 0):
        print("Correct!")
        count = count+1
    else:
        print("No")
    
    print("Congratulation, you got ",count," out of six.")
    print("That is a score of ",count/6," percent.")

```

### 孙从珂 ###

```{code-cell} python3
def quiz():
    correctAnswer = 0
    print("It's quiz time!")
    ###第一个问题
    print("Is Oscar handsome?")
    response1 = input("answer:")
    if (response1 == "yes,he is" or response1 == "yes"):
        print("correct!")
        correctAnswer = correctAnswer + 1
    else:
        print("wrong!")
    ###第二个问题
    print("1+1=?")
    response2 = input("answer:")
    if (response2 == "2"):
        print("correct!")
        correctAnswer = correctAnswer + 1
    else:
        print("wrong!")
    ###第三个问题
    print("who is the best basketball player in the history?")
    response3 = input("answer:")
    if (response3 == "Wilson Ni"):
        print("correct!")
        correctAnswer = correctAnswer + 1
    else:
        print("wrong!")
    ###第四个问题
    print("去年nba总冠军是谁？")
    print("A，勇士")
    print("B，尼克斯")
    print("C，上海大鲨鱼")
    print("D，凯尔特人")
    response4 = input("answer:")
    if (response4 == "A"):
        print("correct!")
        correctAnswer = correctAnswer + 1
    else:
        print("wrong!")
    ###第五个问题
    print("Is CS interesting?")
    response5 = input("answer:")
    if (response5 == "yes"):
        print("correct!")
        correctAnswer = correctAnswer + 1
    else:
        print("wrong!")
    per = correctAnswer / 5 * 100

    print("you have got", correctAnswer, "questions right")
    print("your percentage is", per, "%")
quiz()
```


### 郑好 ###

```{code-cell} python3
#Quiz

score=0

A1=str(input("What is the most incredible manga?"))
if A1=="Gintama" :
    print("Correct!")
else:
    print("Incorrect")
if A1=="Gintama" :
    score=score+20
else:
    score=0


A2=int(input("When was the game 'Ace Attorney Trilogy' first published?"))
if A2==2001:
    print("Correct!")
else:
    print("Incorrect")
if A2==2001:
    score=score+20
else:
    score=score
        

print("What's the most tasty drink? Choose the letter.")
print("A. Coca Cola")
print("B. Spite")
print("C. Pepsi Cola")
print("D. Paraquat")
A3=str(input("What's your answer?"))
if A3=="C":
    print("Correct!")
else:
    print("Incorrect")
if A3=="C":
    score=score+20
else:
    score=score
    

A4=str(input("Which subject is most disgusting?"))
if A4=="Literature":
    print("Correct!")
else:
    print("Incorrect")
if A4=="Literature":
    score=score+20
else:
    score=score
    

A5=int(input("How old am I?"))
if A5==15:
    print("Correct!")
else:
    print("Incorrect")
if A5==15:
    score=score+20
else:
    score=score

print("Your final score is "+str(score)+".")
```

### 吴予纶 ###

```{code-cell} python3
import random

def questions():
    score = 0
    # --- Q1 ---
    month = eval(input('In which month of 2022 is the World cup starting?'))
    if month == 11:
        score += 1
        print('Correct!')
    else:
        print('Incorrect!')
        
    # --- Q2 ---
    choice1 = (input('Who is the basketball god?\nA. Wilson\nB. Ni JiaChen\nC. Grass Fish\nD. Fish\nE. Micheal Jordan'))
    if choice1 == 'E' or choice1 == 'e':
        print('Incorrect! The correct answer is A or B or C or D.')
    else:
        score += 1
        print('Correct')
        
    # --- Q3 ---
    choice2 = (input('Which of the following is a nickname of Jack Xi(奚豪君)?\nA. 肘子\nB. 鲸鱼\nC. 六中哈\nD. 奚比\nE. 科比'))
    if choice2 == 'D' or choice2 == 'd':
        score += 1
        print('Correct!')
    else:
        print('Incorrect! The correct answer is D.')

    # --- Q4 ---
    choice3 = (input('Which of the following is the basketball move Jack Xi(奚豪君) is known for?\nA. 雷霆尬拔\nB. 小抛投\nC. 护球肘\nD. 铁山靠\nE. 闪电五连鞭'))
    if choice3 == 'C' or choice3 == 'c':
        score += 1
        print('Correct!')
    else:
        print('Incorrect! The correct answer is C.')

    # --- Q5 ---
    name = (input('Which teacher is SCLS is a fan of marathon?'))
    if 'pan' in name or 'Pan' in name or '潘' in name or 'saijie' in name or 'Saijie' in name or '赛杰' in name:
        score += 1
        print('Correct!')
    else:
        print('Incorrect! The correct answer is Saijie.')

    finalScore = score / 5
    scoreStr = str(finalScore * 100)
    #print(finalScore, scoreStr)
    print('Congratulations, you got ' + str(score)  + ' answers right.')
    print('That is a score of ' + scoreStr +' percent.')
    
print('--------------------- Quiz ---------------------')
questions()
```

### 费沁沄 ###

```{code-cell} python3
def Quiz_time():
    score=0
    int(score)
    print("quiz time!")
    x=float(input("What is 1*1?"))
    x1=int(x)
    if(x1==1):
        print("Correct")
        score=score+1
    else:
        print("False")
        
    print()
    print("肯德基疯狂星期四V我?")
    print("A:V我50")
    print("B:V我100")
    print("C:V我0")
    print("D:什么是疯狂星期四")
    ans2= input()
    if(ans2=="A"):
        print("Correct")
        score=score+1
    else:
        print("False")
        
    y=float(input("肯德基什么时候成立的?"))
    y1=int(y)
    if(y1==1952):
        print("Correct")
        score=score+1
    else:
        print("False")
    
    print()
    print("麦当劳的吉祥物形象是?")
    print("A:肯德基爷爷")
    print("B:小丑")
    print("C:汉堡人")
    print("D:薯条人")
    ans2= input()
    if(ans2=="B"):
        print("Correct")
        score=score+1
    else:
        print("False")
    
    z=float(input("What is 2/2?"))
    z1=int(z)
    if(z1==1):
        print("Correct")
        score=score+1
    else:
        print("False")
    
    print("Congratulations, you got",score,"question right!")
    score=score/5*100
    print("That is a score of",score,"percent.")
Quiz_time()
```

### 陈楷焜 ###

```{code-cell} python3
def Quiz():
    print("Quiz Time!")
    count = 0
    
    ans1 = int(input("What is 2 + 4? "))
    if(ans1 == 6):
        count += 1
        print("Correct!")
    else:
        print("Incorrect.")
    
    ans2 = input("What city is the Statue of Liberty in? ")
    if(ans2 == "New York"):
        count += 1
        print("Correct!")
    else:
        print("Incorrect.")
    
    ans3 = input("Which country has the largest population in the world? ")
    if(ans3 == "China"):
        count += 1
        print("Correct!")
    else:
        print("Incorrect.")
    
    ans4 = input("How many strings does a violin have? ")
    if(ans4 == "Four" or ans4 == "four" or ans4 == "4"):
        count += 1
        print("Correct!")
    else:
        print("Incorrect.")
    
    ans5 = input("How many Toy Story films are there?\nA.1\nB.2\nC.3\nD.4\n")
    if(ans5 == "D" or ans5 == "d"):
        count += 1
        print("Correct!")
    else:
        print("Incorrect")
    
    print("Congratulations, you got " + str(count) + " answers right.")
    print("That is a score of " + str(count*20) + " percent.")

#Quiz()
```

### 朱启新 ###

```{code-cell} python3
def quiz():
    print("Quiz time!")
    
    print("Q1:What is the result of x when x^0.5=2\n   (a).4  (b).-4  (c).Both a and b  (d).No solution")
    a1=input("Q1:Your answer:")=="a"
    print("Correct!\n" if a1==1 else "No.\n")
    
    print("Q2:What is the number in the units digit of 2022! ?\n   (a).2  (b).4  (c).0  (d).8")
    a2=input("Q2:Your answer:")=="c"
    print("Correct!\n" if a2==1 else "No.\n")
    
    print("Q3:What is the approximate world population in November 2022?\n   (a).80billion  (b).8billion  (c).60billion  (d).800million")
    a3=input("Q3:Your answer:")=="b"
    print("Correct!\n" if a3==1 else "No.\n")
    
    print("Q4:A={1,3,5,7},B={-2,-4,6,-8}. Please figure out the result of '(The complement of (A ∩ B)) ∩ ((The complement of A) ∩  B)' ?\n   (a).A  (b).B  (c).R  (d).{}")
    a4=input("Q4:Your answer:")=="c"
    print("Correct!\n" if a4==1 else "No.\n")
    
    print("Q5:Which is the largest freshwater lake in the world?\n   (a).Caspian Sea  (b).Qinghai Lake  (c).Lake Superior  (d).Black Sea")
    a5=input("Q5:Your answer:")=="c"
    print("Correct!\n" if a5==1 else "No.\n")
    
    a=a1+a2+a3+a4+a5
    if(a==5):
        print("Congratulations!")
    elif(a==4):
        print("Great!")
    elif(a==3):
        print("Not so bad!")
    elif(a==2):
        print("You can be better!")
    elif(a==1):
        print("Keep on fighting!")
    else:
        print("Make persistent efforts!")
    print("You get "+str(a)+" out of 5!")
    print("That is a score of "+str(a/5*100)+" percent.")
print(">>> Quiz")
quiz()
```
### 袁子皓 ###
```{code-cell} python3

an = 0
sco = 0.0
print ('Welcome to Pokemon Test!')
print("Q1:How many evolution types does Eevee have? ")
a = int(input(" "))
if a == 8:
    print("Correct!")
    sco += 25.0
    an += 1
else :
    print("NO!")
print("Q2:What's the number of Pikachu? ")
d = int(input(" "))
if d == 25:
    print("Correct!")
    sco += 25.0
    an += 1
else :
    print("NO!")
print("Q3:The information about Pikachu.Please choose the uncorrect one.")
print("A. Gender ratio 2：1(male:female)")
print("B. Rat Pokémon")
print("C. There are small power bags on either side of the cheek. It discharges when it encounters danger")
b = str(input(""))
if b == "A":
    print("Correct!")
    sco += 25.0
    an += 1
else :
    print("NO!")
print("Q4:What isn't a pokemon's name?")
print("1. Lycanroc")
print("2. Pikachu")
print("3. Charmander")
print("4. Eaceus")
c = int(input(""))
if c == 4:
    print("Correct!")
    sco += 25.0
    an += 1
else :
    print("NO!")
print("Congratulations, you got "+str(an)+" answers right."
"That is a score of "+str(sco)+" percent.")    
```

### 廖恬欣 ###
```{code-cell} python3

def game():
print("GAME LOADING...")
count=0

    print("What is the lower bond of the number?")
    lower_bond=int(input())
    print("What is the upper bond of the number?")
    upper_bond=int(input())
    print("Generating a random number between",lower_bond,"-",upper_bond,"....")
    print("How many tries for the player to win?")
    times=int(input())
    
    print("GAME READY. Now let's play!")
    print("Hello, What's your name?")
    name=input()
    
    print("Hi",name,", you are going to guess a number between",lower_bond,"and",upper_bond,".")
    print("You have",times,"tries to win the game.")
    
    
    import random
    aaa=int(random.randint(lower_bond,upper_bond))
    
    bbb=int(input("Your first guess is:"))
    if(bbb==aaa): 
        print("You win the game in 1 tries!")
    else:
        i=2    
        while(i<=times): 
            if(bbb<aaa):
                print("Your guess is too low")
            else:
                print("Your guess is too high")
            bbb=int(input("Your next guess is:"))
            if(bbb==aaa): 
                print("You win the game in", i,"tries!")
                break  
            else:
                i=i+1   
        if(i>times):
            print("You failed to guess the number within",times,"times,the correct is",aaa)

game()
```

