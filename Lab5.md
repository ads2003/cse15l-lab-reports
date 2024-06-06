# *Lab report 5 ( Putting it all together )*

## *Part 1 – Debugging Scenario*

My goal is to create a procedure that takes an array as input and produces a new array containing every single element from the original array. Rather than publishing the first element in the original array, my code starts printing each element from the second array and skips the first one. I believe there may be an issue with my for loop.This is a screenshot of code.

**Screenshot of the Code:**

<img width="1728" alt="Screenshot 2024-03-11 at 6 17 17 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/ed1ff64d-e668-4eae-963f-518f405b5c3e">

**Symptoms**:

<img width="570" alt="Screenshot 2024-03-12 at 8 34 22 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/14c7e24b-ef8e-4d73-8846-71b1cd714ceb">


## *response of the TA:*

Hey there! Your approach seems OK, however while you're building the new array, try to find any issues in your loop.
When you iterate through the input array, consider how you are accessing the components. Please double check that you are copying each extra element into the result array appropriately! Please let me know what you find.


## *Response of the Student after changes:*

Thank you for the suggestions. Upon closer inspection, I discovered that the code was adding 1 to the correct mean; so, I made the necessary changes to achieve the correct mean.


## *The files and the directory structures:*

<img width="305" alt="Screenshot 2024-03-12 at 8 30 49 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/8211a47d-4929-4dbe-b773-0263c0c50ea0">


## *The Correct Code:*

<img width="493" alt="Screenshot 2024-03-12 at 8 33 38 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/8c2357d3-b7b6-4cba-a636-2b1a26510546">


<img width="739" alt="Screenshot 2024-03-12 at 8 32 27 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/55b98f1a-df42-45a4-8c0f-3f1d6589117d">


## *Description of the edit code :*

I fixed the code by removing the +1 and changing the part where 1 was added to the array length. 


## *Part 2( Reflection)*

In the latter portion of this quarter, I became well-versed in the vim command's editing capabilities. Using this command, I learned how to modify my code in a number of ways and what keys I might press to get different results. 


