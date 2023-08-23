# LeetCode Solutions

---

LeetCode is a popular online platform that provides a collection of coding challenges and problems primarily focused on computer science and programming. It is widely used by individuals, especially those preparing for technical interviews at technology companies, as well as by students and professionals looking to improve their coding and problem-solving skills.

- LeetCode offers a vast array of problems that cover various topics such as data structures (arrays, linked lists, trees, graphs, etc.) and algorithms (sorting, searching, dynamic programming, etc.). These problems are designed to challenge users' ability to write efficient and correct code to solve specific tasks or puzzles.

- Users can submit their solutions to the problems using various programming languages like Python, Java, C++, and more. LeetCode then evaluates the submissions for correctness, efficiency, and runtime performance. This allows users to practice coding, learn new techniques, and improve their skills by tackling a diverse set of problems.

- The platform also includes features such as a discussion forum for problem-solving discussions, articles and solutions contributed by the community, and premium features for more personalized practice and learning experiences.

---


## **1. Rotate Array in Java**

You may have been using Java for a while. Do you think a simple Java array question
can be a challenge? Let’s use the following problem to test.

Problem: Rotate an array of n elements to the right by k steps. For example, with n = 7 and k = 3, the array [1,2,3,4,5,6,7] is rotated to [5,6,7,1,2,3,4].
How many different ways do you know to solve this problem?


##### **Solution 1 - Intermediate Array**

```
In a straightforward way, we can create a new array and then copy elements to the
new array. Then change the original array by using System.arraycopy().


public void rotate(int[] nums, int k) {
 if(k > nums.length)
 k=k%nums.length;
 int[] result = new int[nums.length];
 for(int i=0; i < k; i++){
   result[i] = nums[nums.length-k+i];
 }
 int j=0;
 for(int i=k; i<nums.length; i++){
   result[i] = nums[j];
   j++;
 }
 System.arraycopy( result, 0, nums, 0, nums.length );
}

Space is O(n) and time is O(n).

```


##### **Solution 2 - Bubble Rotate** 

```
Can we do this in O(1) space?
  This solution is like a bubble sort

public static void rotate(int[] arr, int order) {
	if (arr == null || order < 0) {
		throw new IllegalArgumentException("Illegal argument!");
	}

	for (int i = 0; i < order; i++) {
		for (int j = arr.length - 1; j > 0; j--) {
			int temp = arr[j];
			arr[j] = arr[j - 1];
			arr[j - 1] = temp;
		}
	}
}

However, the time is O(n*k).

```

##### **Solution 3 - Reversal**

```
Can we do this in O(1) space and in O(n) time? The following solution does.
Assuming we are given 1,2,3,4,5,6 and order 2. The basic idea is:

  1. Divide the array two parts: 1,2,3,4 and 5, 6
  2. Rotate first part: 4,3,2,1,5,6
  3. Rotate second part: 4,3,2,1,6,5
  4. Rotate the whole array: 5,6,1,2,3,4

--------------------

public static void rotate(int[] arr, int order) {
	order = order % arr.length;

	if (arr == null || order < 0) {
		throw new IllegalArgumentException("Illegal argument!");
	}

	//length of first part
	int a = arr.length - order;

	reverse(arr, 0, a-1);
	reverse(arr, a, arr.length-1);
	reverse(arr, 0, arr.length-1);
}

public static void reverse(int[] arr, int left, int right) 
{
	if(arr == null || arr.length == 1)
		return;

	while(left < right){
		int temp = arr[left];
		arr[left] = arr[right];
		arr[right] = temp;
		left++;
		right--;
	}
}

```

## **2. Evaluate Reverse Polish Notation**

The problem:

Evaluate the value of an arithmetic expression in Reverse Polish Notation.
Valid operators are +, -, *, /. Each operand may be an integer or another
expression.

Some examples:

["2", "1", "+", "3", "*"] -> ((2 + 1) * 3) -> 9

["4", "13", "5", "/", "+"] -> (4 + (13 / 5)) -> 6

##### **Solution 1 - Naive Approach**

```
This problem is simple. After understanding the problem, we should quickly realize
that this problem can be solved by using a stack. We can loop through each element
in the given array. When it is a number, push it to the stack. When it is an operator,
pop two numbers from the stack, do the calculation, and push back the result.

The following is the code. It runs great by feeding a small test. However, this code contains
compilation errors in leetcode. Why?

public class Test {
	public static void main(String[] args) throws IOException {
		String[] tokens = new String[] { "2", "1", "+", "3", "*" };
		System.out.println(evalRPN(tokens));
	}

public static int evalRPN(String[] tokens) {
	int returnValue = 0;
	String operators = "+-*/";

	Stack<String> stack = new Stack<String>();

	for (String t : tokens) {
		if (!operators.contains(t)) {
			stack.push(t);
		} else {
			int a = Integer.valueOf(stack.pop());
			int b = Integer.valueOf(stack.pop());
			switch (t) {
			  case "+":
				stack.push(String.valueOf(a + b));
				break;
			  case "-":
				stack.push(String.valueOf(b - a));
				break;
			  case "*":
				stack.push(String.valueOf(a * b));
				break;
			  case "/":
				stack.push(String.valueOf(b / a));
				break;
			}
		}
	}
	returnValue = Integer.valueOf(stack.pop());
	return returnValue;
	}
}

The problem is that switch string statement is only available from JDK 1.7. Leetcode
apparently use versions below that.

```

##### **Solution 2 - Accepted Solution**

```
If you want to use switch statement, you can convert the above by using the following
code which use the index of a string "+-*/".

public class Solution {
	public int evalRPN(String[] tokens) {
		int returnValue = 0;
		String operators = "+-*/";

		Stack<String> stack = new Stack<String>();

		for(String t : tokens){
			if(!operators.contains(t)){
				stack.push(t);
			}else{
				int a = Integer.valueOf(stack.pop());
				int b = Integer.valueOf(stack.pop());
				int index = operators.indexOf(t);
				switch(index){
					case 0:
						stack.push(String.valueOf(a+b));
						break;
					case 1:
						stack.push(String.valueOf(b-a));
						break;
					case 2:
						stack.push(String.valueOf(a*b));
						break;
					case 3:
						stack.push(String.valueOf(b/a));
						break;
				}
			}
		}
	returnValue = Integer.valueOf(stack.pop());
	return returnValue;
	}
}


```

## **3. Solution of Longest Palindromic Substring in Java**

Finding the longest palindromic substring is a classic problem of coding interview. In
this post, I will summarize 3 different solutions for this problem

##### **Solution 1 - Naive Approach**

```
Naively, we can simply examine every substring and check if it is palindromic. The
time complexity is O(n3ˆ). If this is submitted to LeetCode onlinejudge, an error message will be returned - "Time Limit Exceeded". Therefore, this approach is just a start,
we need a better algorithm.

public static String longestPalindrome1(String s) {
	int maxPalinLength = 0;
	String longestPalindrome = null;
	int length = s.length();

	// check all possible sub strings
	for (int i = 0; i < length; i++) {
		for (int j = i + 1; j < length; j++) {
			int len = j - i;
			String curr = s.substring(i, j + 1);
			if (isPalindrome(curr)) {
				if (len > maxPalinLength) {
					longestPalindrome = curr;
					maxPalinLength = len;
				}
			}
		}
	}
	return longestPalindrome;
}

public static boolean isPalindrome(String s) {
	for (int i = 0; i < s.length() - 1; i++) {
		if (s.charAt(i) != s.charAt(s.length() - 1 - i)) {
			return false;
		}
	}
	return true;
}

```

##### **Solution 2 - Dynamic Programming**

```
Let s be the input string, i and j are two indices of the string.
Define a 2-dimension array "table" and let table[i][j] denote whether substring from
i to j is palindrome.

Start condition:

	table[i][i] == 1;
	table[i][i+1] == 1 => s.charAt(i) == s.charAt(i+1)

Changing condition:

	table[i+1][j-1] == 1 && s.charAt(i) == s.charAt(j) => table[i][j] == 1

Time O(n2ˆ) Space O(n2ˆ)

--------------------------------------------------------------------

public static String longestPalindrome2(String s) {
	if (s == null)
		return null;

	if(s.length() <=1)
			return s;

	int maxLen = 0;
	String longestStr = null;

	int length = s.length();

	int[][] table = new int[length][length];

	//every single letter is palindrome
	for (int i = 0; i < length; i++) {
		table[i][i] = 1;
	}

	printTable(table);

	//e.g. bcba
	//two consecutive same letters are palindrome
	for (int i = 0; i <= length - 2; i++) {
		if (s.charAt(i) == s.charAt(i + 1)){
			table[i][i + 1] = 1;
			longestStr = s.substring(i, i + 2);
		}
	}

	printTable(table);

	//condition for calculate whole table
	for (int l = 3; l <= length; l++) {
		for (int i = 0; i <= length-l; i++) {
			int j = i + l - 1;
			if (s.charAt(i) == s.charAt(j)) {
				table[i][j] = table[i + 1][j - 1];
				if (table[i][j] == 1 && l > maxLen)
					longestStr = s.substring(i, j + 1);
				} else {
					table[i][j] = 0;
				}
				printTable(table);
		}
	}
	return longestStr;
}

public static void printTable(int[][] x){
	for(int [] y : x){
		for(int z: y){
			System.out.print(z + " ");
		}
		System.out.println();
	}
	System.out.println("------");
}

Given an input, we can use printTable method to examine the table after each iteration. For example,
 if input string is "dabcba", the final matrix would be the following:

1 0 0 0 0 0
0 1 0 0 0 1
0 0 1 0 1 0
0 0 0 1 0 0
0 0 0 0 1 0
0 0 0 0 0 1


From the table, we can clear see that the longest string is in cell table[1][5].

```

##### **Solution 3 - Simple Algorithm**

```
Time O(n2ˆ), Space O(1)

---------------------------------------------------------

public String longestPalindrome(String s) {
	if (s.isEmpty()) {
		return null;
	}

	if (s.length() == 1) {
	return s;
	}

	String longest = s.substring(0, 1);

	for (int i = 0; i < s.length(); i++) {
		// get longest palindrome with center of i
		String tmp = helper(s, i, i);

		if (tmp.length() > longest.length()) {
			longest = tmp;
		}

		// get longest palindrome with center of i, i+1
		tmp = helper(s, i, i + 1);
		if (tmp.length() > longest.length()) {
			longest = tmp;
		}
	}
	return longest;
}

// Given a center, either one letter or two letter,
// Find longest palindrome
public String helper(String s, int begin, int end) {
	while (begin >= 0 && end <= s.length() - 1 && s.charAt(begin) == s.charAt(end)) {
		begin--;
		end++;
	}
	return s.substring(begin + 1, end);
}

```

## **4. Solution Word Break**

Given a string s and a dictionary of words dict, determine if s can be segmented into a space-separated sequence of one or more dictionary words. For example, given s = "leetcode", dict = ["leet", "code"]. Return true because "leetcode" can be segmented as "leet code".

##### **Solution 1 - Naive Approach**

```
This problem can be solve by using a naive approach, which is trivial. A discussion
can always start from that though.

------------------------------------------------------------

public class Solution {

    public boolean wordBreak(String s, Set<String> dict) {
        return wordBreakHelper(s, dict, 0);
    }

    private boolean wordBreakHelper(String s, Set<String> dict, int start) {
        if (start == s.length()) {
            return true;
        }

        for (String word : dict) {
            int len = word.length();
            int end = start + len;

            if (end > s.length()) {
                continue;
            }

            if (s.substring(start, end).equals(word)) {
                if (wordBreakHelper(s, dict, end)) {
                    return true;
                }
            }
        }

        return false;
    }
}


Time: O(n2ˆ)
This solution exceeds the time limit.


```

##### **Solution 2 - Dynamic Programming**

```
The key to solve this problem by using dynamic programming approach:

	• Define an array t[] such that t[i]==true =>0-(i-1) can be segmented using dictionary
	• Initial state t[0] == true

--------------------------------------------------------------
public class Solution {

    public boolean wordBreak(String s, Set<String> dict) {
        boolean[] t = new boolean[s.length() + 1];

        // set first to be true, why?
        // Because we need initial state
        t[0] = true;

        for (int i = 0; i < s.length(); i++) {
            // should continue from match position
            if (!t[i]) {
                continue;
            }

            for (String a : dict) {
                int len = a.length();
                int end = i + len;

                if (end > s.length()) {
                    continue;
                }

                if (t[end]) {
                    continue;
                }

                if (s.substring(i, end).equals(a)) {
                    t[end] = true;
                }
            }
        }

        return t[s.length()];
    }
}

--------------------------------------------------------------

Time: O(string length * dict size)
One tricky part of this solution is the case:

	INPUT: "programcreek", ["programcree","program","creek"].

We should get all possible matches, not stop at "programcree".
```

##### **Solution 3 -  Regular Expression**

```
The problem is supposed to be equivalent to matching the regexp (leet|code)*, which
means that it can be solved by building a DFA in O(2m) and executing it in O(n). ˆ
Leetcode online judge does not allow using Pattern class though.

--------------------------------------------------------------
public class Main {

    public static void main(String[] args) {
        HashSet<String> dict = new HashSet<>();
        dict.add("go");
        dict.add("goal");
        dict.add("goals");
        dict.add("special");

        StringBuilder sb = new StringBuilder();
        for (String s : dict) {
            sb.append(s).append("|");
        }

        String pattern = sb.toString().substring(0, sb.length() - 1);
        pattern = "(" + pattern + ")*";
        Pattern p = Pattern.compile(pattern);
        Matcher m = p.matcher("goalspecial");

        if (m.matches()) {
            System.out.println("match");
        }
    }
}

--------------------------------------------------------------

```

## **5. Word Break II**

Given a string s and a dictionary of words dict, add spaces in s to construct a sentence
where each word is a valid dictionary word. Return all such possible sentences.
For example, given s = "catsanddog", dict = ["cat", "cats", "and", "sand", "dog"], the
solution is ["cats and dog", "cat sand dog"].

##### **Solution 1 - Dynamic Programming**

```
This problem is very similar to Word Break. Instead of using a boolean array to track
the match positions, we need to track the actual words. Then we can use depth first
search to get all the possible paths, i.e., the list of strings.

--------------------------------------------------------------

public static List<String> wordBreak(String s, Set<String> dict) {

    // create an array of ArrayList<String>
    List<String>[] dp = new ArrayList[s.length() + 1];
    dp[0] = new ArrayList<String>();

    for (int i = 0; i < s.length(); i++) {
        if (dp[i] == null) {
            continue;
        }

        for (String word : dict) {
            int len = word.length();
            int end = i + len;

            if (end > s.length()) {
                continue;
            }

            if (s.substring(i, end).equals(word)) {
                if (dp[end] == null) {
                    dp[end] = new ArrayList<String>();
                }
                dp[end].add(word);
            }
        }
    }

    List<String> result = new LinkedList<String>();
    if (dp[s.length()] == null) {
        return result;
    }

    ArrayList<String> tmp = new ArrayList<>();
    dfs(dp, s.length(), result, tmp);
    return result;
}

public static void dfs(List<String>[] dp, int end, List<String> result, ArrayList<String> tmp) {

    if (end <= 0) {
        String path = tmp.get(tmp.size() - 1);
        for (int i = tmp.size() - 2; i >= 0; i--) {
            path += " " + tmp.get(i);
        }
        result.add(path);
        return;
    }

    for (String str : dp[end]) {
        tmp.add(str);
        dfs(dp, end - str.length(), result, tmp);
        tmp.remove(tmp.size() - 1);
    }
}


--------------------------------------------------------------

```
