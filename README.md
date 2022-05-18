# Revature weekly code challenges
## Challenge 05/16/2022 - 05/20/2022

## Sum List
![sumListSol](https://user-images.githubusercontent.com/40347155/169075595-13e93f7f-ddef-42b9-adc6-0e00c9b98ca6.JPG)
```
import java.util.*;

class Solution {
  public static void main(String[] args) {
    List<Integer> listOne = new LinkedList<>();
    listOne.add(1);
    listOne.add(2);
    listOne.add(3);
    listOne.add(4);
    List<Integer> listTwo = new LinkedList<>();
    listTwo.add(2);
    listTwo.add(3);
    listTwo.add(4);
    listTwo.add(5);

    StringBuilder firstNumber = new StringBuilder();
    StringBuilder secondNumber = new StringBuilder();

    listOne.forEach(digit -> {
      firstNumber.append(digit.toString());
    });
    listTwo.forEach(digit -> {
      secondNumber.append(digit.toString());
    });

    firstNumber.reverse();
    secondNumber.reverse();
    System.out.printf("%s + %s = ", firstNumber.toString(), secondNumber.toString());
    System.out.println(Integer.valueOf(firstNumber.toString()) + Integer.valueOf(secondNumber.toString()));
```

##Stack Sol
![stackSol](https://user-images.githubusercontent.com/40347155/169075619-61a62107-56c4-4395-9e97-cdde0010fe61.JPG)
```
import java.util.*;

class Solution {
  public static void main(String[] args) {

    Stack<Integer> regularStack = new Stack<Integer>();
    regularStack.push(1);
    regularStack.push(2);
    regularStack.push(3);
    regularStack.push(4);
    regularStack.push(5);
    regularStack.push(4);

    int minValue = regularStack.peek();
    String stackAsString = regularStack.toString();
    String normalizedStackAsString = stackAsString.substring(1, stackAsString.length() - 1);
    String stackArr[] = normalizedStackAsString.split(", ");

    for (int i = 0 ; i < stackArr.length; i++) {
      int tempMin = Integer.parseInt(stackArr[i]);
      if (tempMin < minValue) {
        minValue = tempMin;
      }
    }
    System.out.println(minValue);
  }
}
```
