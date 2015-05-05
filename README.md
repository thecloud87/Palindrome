# Palindrome
#checks to see if a word is a palindrome

import unittest

def palindrome(word):
    palindrome_check = []
    for c in word[::-1]:
        palindrome_check.append(c)
    print(palindrome_check)
    drow = ''.join(palindrome_check)
    print(drow)
    if drow == word:
        return True
    else:
        return False

palindrome("racecar")

#2 assert tests true/false

class myTest(unittest.TestCase):
    def test_palindrome_is_true(self):
        self.assertTrue(palindrome("racecar"), True)

    def test_palindrome_is_false(self):
        self.assertFalse(palindrome("mother"), False)

unittest.main()
