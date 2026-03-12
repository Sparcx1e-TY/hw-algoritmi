"""
ТИП 2 - ЗАДАЧИ
"""

# 
# Задача 18578
# 


    for x in range(2):
        for y in range(2):
            for z in range(2):
                for w in range(2):
                    part1 = x and (not y)
                    part2 = (not w) or z
                    left = part1 or part2
                    right = 1 if (z == x) else 0
                    f = 1 if (left == right) else 0
                    print(f"{x}{y}{z}{w}{f}")


# 
# Задача 84696
# 


    for w in range(2):
        for x in range(2):
            for z in range(2):
                for y in range(2):
                    part1 = (not w) or y
                    part2 = (not z) or x
                    part3 = part2 or z
                    f = 1 if ((not part1) or part3) else 0
                    print(f"{w}{x}{z}{y}{f}")



#
# Задача 18781
#


    for x in range(2):
        for y in range(2):
            for z in range(2):
                for w in range(2):
                    part1 = (not x) or (not y)
                    part2 = 1 if ((not x) == z) else 0
                    f = part1 and part2 and w
                    f = 1 if f else 0
                    if f == 1:
                        print(f"{x}{y}{z}{w}{f}")


"""
ТИП 8 - ЗАДАЧИ
"""

# 
# Задача 26953
# 


    k = 0
    for a in range(1, 8):
        for b in range(0, 8):
            for c in range(0, 8):
                for d in range(0, 8):
                    for e in range(0, 8):
                        if len({a,b,c,d,e}) == 5:
                            if a%2 != b%2 and b%2 != c%2 and c%2 != d%2 and d%2 != e%2:
                                k = k + 1
    
    print(f"Количество чисел: {k}")


# 
# Задача 60250
# 


    k = 0
    for a in range(1, 8):
        for b in range(0, 8):
            for c in range(0, 8):
                for d in range(0, 8):
                    for e in range(0, 8):
                        if 1 not in {a,b,c,d,e} and len({a,b,c,d,e}) == 5:
                            if a%2 != b%2 and b%2 != c%2 and c%2 != d%2 and d%2 != e%2:
                                k = k + 1
    
    print(f"Количество чисел: {k}")
