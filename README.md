# python-interactive-program
#python interactive program for star pattern
print("enter q to quit the program\n")
program_over = False
while program_over is False:
    l = input("How many rows you want to print:\n")
    if l == "q":
        program_over = True
    else:
        print("\n code of star pattern\n")

        m = int(input("enter 0 for decreasing and 1 for increasing\n"))
        n = int(l)
        o = n + 1
        def convert_bool(_bool):
            if _bool == 1:
                return True
            elif _bool == 0:
                return False
        if n < 0:
            print("you have enter negative value")
        else:
            if m == 0 or m == 1:
                if convert_bool(m):
                    print("\n * pattern in ascending order")
                    for times in range(o):
                        print("*" * times)
                elif not convert_bool(m):
                    print("\n * pattern in descending order")
                    while n >= 1:
                        print("*" * n)
                        n = n - 1
                else:
                    print("sorry you have to input only 0 or 1")
