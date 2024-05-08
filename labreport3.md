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
