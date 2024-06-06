# *Lab report 5 ( Putting it all together )*

## *Part 1 – Debugging Scenario*

My goal is to create a procedure that takes an array as input and produces a new array containing every single element from the original array. Rather than publishing the first element in the original array, my code starts printing each element from the second array and skips the first one. I believe there may be an issue with my for loop.This is a screenshot of code.

**Screenshot of the Code:**

<img width="834" alt="Screenshot 2024-06-05 at 6 20 39 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/d3e61bdd-8f30-423f-9d4a-22c8c2fc8bc7">


**Symptoms**:

<img width="458" alt="Screenshot 2024-06-05 at 6 20 49 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/3cedd9f1-e3b6-4943-95cc-62b9f74414a2">


## *response of the TA:*

Hey there! Your approach seems OK, however while you're building the new array, try to find any issues in your loop.
When you iterate through the input array, consider how you are accessing the components. Please double check that you are copying each extra element into the result array appropriately! Please let me know what you find.


## *Response of the Student after changes:*

Thank you for the suggestions. Upon closer inspection, I discovered that the code was adding 1 to the correct mean; so, I made the necessary changes to achieve the correct mean.


## *The files and the directory structures:*

<img width="287" alt="Screenshot 2024-06-05 at 6 20 54 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/e0b38b0f-913e-4533-b95e-3118875e2f36">


## *The Correct Code:*

<img width="562" alt="Screenshot 2024-06-05 at 6 21 13 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/71709f9a-bc06-4956-bc08-15d9a91597db">

<img width="477" alt="Screenshot 2024-06-05 at 6 21 02 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/ddf080fb-b0d4-474c-912e-828ab8ce1f21">


## *Description of the edit code :*

I fixed the code by removing the +1 and changing the part where 1 was added to the array length. 


## *Part 2( Reflection)*

In the latter portion of this quarter, I became well-versed in the vim command's editing capabilities. Using this command, I learned how to modify my code in a number of ways and what keys I might press to get different results. 


