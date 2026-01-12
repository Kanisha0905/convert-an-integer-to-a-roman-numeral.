# convert-an-integer-to-a-roman-numeral.
class RomanSolution:
    @staticmethod
    def int_to_Roman(num):
        val = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1]
        syb = ["M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"]
        roman_num = ""  # Corrected the quotes here
        i = 0
        if num < 1 or num > 3999:
            print("ENTER A GOOD VALUE!")
            return None  # Add a return to avoid proceeding with invalid input
        else:
            while num > 0:
                if num >= val[i]:
                    roman_num += syb[i]
                    num -= val[i]
                else:
                    i += 1
            return roman_num


# Driver code
n = int(input("ENTER A NUMBER: "))
result = RomanSolution.int_to_Roman(n)
if result:
    print("Roman numeral of given number is:", result)
ENTER A NUMBER: 500
Roman numeral of given number is: D
