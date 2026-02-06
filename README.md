# KSA-basic-mission1

#####################################
#       Basic Mission #1
#       신호등 컨트롤러 설계
#####################################


#start

mode = input('mode를 선택하세요.\n 1: normal mode \n 2: monitor mode\n')

if mode == 1:   #normal mode
    print('normal mode')
elif mode == 2: #monitor mode
    print('[monitor mode]\n')
    cnum = input('write the cycle numer: ')
    

clrstate = ['green', 'yellow', 'left', 'red', 'blink']
cycle = 0
count = 0

for i in range(70):
    cycle += 1


def CarTraffic():
    for j in range(70):
        count += 1

        clrstate = 'green'

        if clrstate == 'green':
            if count >= 20:
                clrstate = 'yellow'
                count = 0
        
        if clrstate == 'yellow':
            if count >= 2:
                clrstate = 'left'
                count = 0

        if clrstate == 'left':
            if count >= 10:
                clrstate = 'yellow'
                count = 0
        
        if clrstate == 'yellow':
            if count >= 2:
                clrstate = 'red'
                count = 0

        if clrstate == 'red':
            if count >= 34:
                clrstate = 'green'
                count = 0
    



def HumanTraffic():
    for k in range(70):
        count = 0

        clrstate = 'red'

        if clrstate == 'red':
            if count >= 34:
                clrstate = 'green'
                count = 0
        
        if clrstate == 'green':
            if count >= 14:
                clrstate = 'blink'
                count = 0

        if clrstate == 'blink':
            if count >= 6:
                clrstate = 'red'
                count = 0

        if clrstate == 'red':
            if count >= 14:
                clrstate = 'red'
                count = 0


    

if start == 'start':
    CarTraffic()
    HumanTraffic()





