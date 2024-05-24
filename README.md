#ans0
1
Microsoft Windows [版本 10.0.19045.2965]
(c) Microsoft Corporation. 著作權所有，並保留一切權利。

C:\Users\user>python --version
Python 3.7.0
2
Microsoft Windows [版本 10.0.19045.2965]
(c) Microsoft Corporation. 著作權所有，並保留一切權利。

C:\Users\user>cmd
Microsoft Windows [版本 10.0.19045.2965]
(c) Microsoft Corporation. 著作權所有，並保留一切權利。

C:\Users\user>where python
C:\Users\user\AppData\Local\Programs\Python\Python37\python.exe
#ans1
pattern = "*+"
# 定義圖案，即"*+"。
for i in range(10):
    # 進入一個循環，執行10次，用於輸出10行。
    
    if i % 2 == 0:
        # 如果行數為偶數（從0開始），執行以下代碼。
        
        print(pattern * 10)
        # 輸出一行，由pattern乘以10組成。
        
    else:
        # 如果行數為奇數，執行以下代碼。
        
        print(pattern[::-1] * 10)
        # 輸出一行，由pattern反轉後乘以10組成。

#ans2
n = int(input())  # 讀取第一行，表示隊伍的數量
team_counts = [int(input()) for _ in range(n)]  # 讀取每個隊伍的人數並存入列表

valid_teams = 0  # 初始化合法隊伍數量為0

# 迴圈遍歷每個隊伍的人數
for count in team_counts:
    # 如果隊伍人數是3的倍數且不為0，則該隊伍為合法隊伍
    if count % 3 == 0 and count != 0:
        # 將合法隊伍數量加1
        valid_teams += 1

print(valid_teams)  # 輸出合法隊伍數量

#ans3
# 自我介绍

## 关于我

我是(陳品伃)[https://github.com/pinyu1012]，是一名(學生)。我对 (音樂) 非常感兴趣，并且致力于在这方面取得进步。

## 联系方式

- GitHub: (pinyu1012)[https://github.com/pinyu1012]
- 邮箱: pennychen1012@gmail.com

#ans4
import random

def guess_number(x1, x2, n):
    # 随机生成目标数字
    target_number = random.randint(x1, x2)
    
    # 初始化猜测次数
    guesses_taken = 0
    
    # 提示游戏开始
    print(f"猜测一个在 {x1} 到 {x2} 之间的数字！")
    
    # 开始游戏循环
    while guesses_taken < n:
        guess = int(input("你的猜测："))
        guesses_taken += 1
        
        # 判断猜测是否正确
        if guess == target_number:
            print(f"恭喜你，猜对了！目标数字是 {target_number}。")
            break
        elif guess < target_number:
            print("太低了！再试试吧。")
        else:
            print("太高了！再试试吧。")
    
    # 如果猜测次数用尽仍未猜中，显示失败信息
    if guesses_taken == n and guess != target_number:
        print(f"很遗憾，你没有在 {n} 次内猜中目标数字。它是 {target_number}。")

# 测试游戏
guess_number(1, 100, 5)








