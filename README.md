import random
def welcome():
    for i in range(0,20):
        print("*\t",end="")
    print()
    print("*",end="")
    for i in range(0,19):
        print("\t",end="")
    print("*")
    print()
    print("*",end="")
    for i in range(0,19):
        print("\t",end="")
    print("*")
    print()
    print("*",end="")
    for i in range(0,5):
        print("\t",end="")
    print("welcome to world best fun game",end="")
    for i in range(0,8):
        print("\t",end="")
    print("*")
    print()
    print("*",end="")
    for i in range(0,19):
        print("\t",end="")
    print("*")
    print()
    print("*",end="")
    for i in range(0,19):
        print("\t",end="")
    print("*")
    print()
    for i in range(0,20):
        print("*\t",end="")
    print("\n","created by SHUBHAM KUMAR")
    print()
    input("press any key to start:")
welcome()
print("\n"*100)

def mainmenu():
    print("1.Rock paper scissor\n2.cows and bulls\n3.exit")
    ch=int(input("Enter your choice number:"))
    if ch==1:
       rockpaperscissormenu()
    elif ch==2:
        cowsandbullsmenu()
    elif ch==3:
        exit()
    else:
      print("invalid choice")
      mainmenu()
def rockpaperscissormenu():
    print("1.play\n2.rules\n3.return to main menu")
    ch = int(input("Enter your choice number:"))
    if ch == 1:
        rockpaperscissors()
    elif ch == 2:
        rockpaperscissorrules()
    elif ch == 3:
        mainmenu()
    else:
        print("invalid choice")
        rockpaperscissormenu()
def cowsandbullsmenu():
    print("1.play\n2.rules\n3.return to main menu")
    ch = int(input("Enter your choice number:"))
    if ch == 1:
        cowsandbulls()
    elif ch == 2:
        cowsandbullsrules()
    elif ch == 3:
        mainmenu()
    else:
        print("invalid choice")
        cowsandbullsmenu()
def rockpaperscissors():
    print("WELCOME TO ROCK PAPER AND SCISSORS")
    print("you will be competing against the computer.the player that score 5 points first, will be decellared as the winner.")
    print("if your choice is rock, please enter 0.")
    print("if your choice is paper, please enter 1.")
    print("if your choice is scissor, please enter 2.")
    print("if you wish to exit, please enter -1.")
    user=0
    comp=0
    cnt=0
    chc=["rock","paper","scissor"]
    while (user<5 and comp<5 and cnt<50):
        cnt+=1
        u_ch=int(input("Enter you choice:"))
        if u_ch==-1:
            print("thank you")
            return
        c_ch=random.choice([0,1,2])
        if u_ch==0 and c_ch==1:
            comp+=1
        elif u_ch==0 and c_ch==2:
            user+=1
        elif u_ch==1 and c_ch==0:
            user+= 1
        elif u_ch==1 and c_ch==2:
            comp+= 1
        elif u_ch==2 and c_ch==0:
            comp+= 1
        elif u_ch==2 and c_ch==1:
            user+= 1
        print("you:",chc[u_ch])
        print("comp:",chc[c_ch])
        print(("your score:",user,"\t computer's score:",comp))
    if(user>comp):
        print("congratulation! you win")
    elif(comp>user):
        print("Oops! sorry you loose.Better luck next time!")
    else:
        print("Match draw.")
    mainmenu()
def rockpaperscissorrules():
    print('''
                    'Rock Paper Scissors is a zero sum game that is usually played by two people using their hands and no tools.The idea is to make shapes with an outstretched hand where each shape will have a certain degree of power and will lead to an outcome.What are the rules of RPS?'
                    'Although the game has a lot of complexity to it, the rules to play it are pretty simple.The game is played where players deliver hand signals that will represent the elements of the game; rock, paper and scissors. The outcome of the game is determined by 3 simple rules:'
                    '1.Rock wins against scissors.'
                    '2.Scissors win against paper.'
                    '3.Paper wins against rock.'
                    'The Hand Signals'
                    'In order to ensure fair play, the game signals have been agreed upon to ensure the uniformity of delivery every single time. This ensures that there will be no room for error and these signals have been approved for all types of recreational and professional play.'
                    'The proper opening move will impact the overall success of the game. This means that special attention should be given to the way you move your hand initially before you attempt to make any signal so that other players are not aware of your intention. When you succeed to do so, you ensure that other players will not be able to make a signal that beats yours, at least not on purpose.'
                    'The Rock'
                    'The rock is internationally recognized by a closed fist where the thumb is not concealed. It is also one of the most popular opening moves and this is why it is considered to be one of the most popular hand signals. Most players will view using the rock as an opening move to be somehow aggressive but would still use it because it is easy. The rock will beat scissors every time but will be beaten by paper.'
                    'The Paper'
                    'Paper is delivered in the same way as the rock except that in this case all the fingers and the thumb are extended in a way that they all face the same direction. The vertical paper or the handshake is strictly forbidden in tournaments of Rock Paper Scissors because it might resemble the scissors which can lead to unnecessary confusion. Paper is one of the most challenging opening moves because there is no indication of what you intend to do next. As a result, many players will be concerned when you use it as an opening move to your game. Paper will beat rock but will be beaten by scissors in no time.'
                    'The Scissors'
                    'Scissors are thrown in the same way as rock where the hand is clenched into a fist but the index and the middle finger are extended to the front in order to make an angle that is of 30 to 45 degrees in a way that would resemble a pair of scissors. The use of horizontal scissors is strictly forbidden in tournaments because they can resemble the shape of paper. Opening with scissors is not a very smart move because your opponent will be able to guess what your signal is going to be easily and so will be able to come up with a stronger signal.'
                    'It is very important to conceal your move and to surprise your opponent if you want to make sure that you will win this game.
                    ''')
    mainmenu()
def cowsandbulls():
    print("Welcome to cows and bulls game")
    words=["calm","loss","wins","fail","rate","cake","time","face","tear","sore"]
    rand=random.randrange(0,10)
    word=words[rand]
    cnt=0
    while(cnt<15):
        s=input("Enter string:")
        if s=="-1":
            print("Thank you!")
            return
        cows=0
        bulls=0
        chars=0
        for c in s:
            if c in word:
                chars+=1
        for i in range(0,4):
            if s[i]==word[i]:
                bulls+=1
        cows=("Cows:",cows,"\tBulls",bulls)
        if bulls==4:
            print("Congratulations! you win!")
            mainmenu()
        cnt+=1
    print("Oops! maximum guess limit reached!")
    mainmenu()
def cowsandbullsrules():
    print(' ' ' '
          'On a sheet of paper the players, each write a four digit secret number.''\n'
          'The digits must be all different. Then, in turn, the players try to guess their opponents number who gives the number of matches.''\n'
          'if the matching digits are in their right positions, they are "bulls", if in different positions,they are "cows.''\n'
          'Rules:''\n'
          'All digits in the secret number are different.''\n'
          'The secret number cannot start with zero.''\n'
          'If your try has matching digits on the exact places, they are Bulls.''\n'
          'If you have digits from the secret number, but not on the right places, they are Cows.''\n'
          'In the lower text area is added your proposition and the number of bulls and cows that match.' ' ')
    mainmenu()
mainmenu()















