# Lab Report 3 - Bugs and Commands


## *Part 1(Bugs)*

Inputs that induce failiure

```
import static org.junit.Assert.assertArrayEquals;

public class TestReverseInPlace {
    @org.junit.Test
    public void testReverseInPlace() {
        int[] input1 = {3, 4, 5};
        ArrayExamples.reverseInPlace(input1);
        assertArrayEquals(new int[]{5, 4, 3}, input1);
    }
}
```
Inputs that does not cause failure

```
import static org.junit.Assert.assertArrayEquals;

public class TestReverseInPlace {
    @org.junit.Test
    public void testReverseInPlace() {
        int[] input1 = {3};
        ArrayExamples.reverseInPlace(input1);
        assertArrayEquals(new int[]{3}, input1);
    }
}
```

## *Symptoms*


<img width="556" alt="Screenshot 2024-05-08 at 3 06 35 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/7664e73c-58cb-4940-9182-e569f5c6b82e">


*Before fixing bug*

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```


*After fixing bug*

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```


## *Part 2(Researching commands)*
