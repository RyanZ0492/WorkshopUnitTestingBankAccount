Extra Workshop: Unit Testing with Visual Studio
For the extra workshop, I followed the article “Walkthrough: Create and run unit tests for managed code” from Microsoft Learn. This workshop helped me understand how to write and run unit tests for C# code using Visual Studio.

First, I created a new Console App project in Visual Studio and named it Bank. In this project, I made a class called BankAccount that lets you add and remove money from a balance. Then I added a second project to the solution, called BankTests, using the MSTest Test Project template. I linked the test project to the Bank project, so I could test its methods.

Next, I renamed the default test class to BankAccountTests and added a using statement to work with the BankAccount class. I wrote a test method called Debit_WithValidAmount_UpdatesBalance. This test checks if the Debit method correctly updates the account balance when a valid amount is taken out. However, the test failed at first. After checking the code, I saw that the Debit method was adding money instead of subtracting it. I fixed this mistake by changing m_balance += amount; to m_balance -= amount;.

After fixing the bug, I ran the test again, and it passed. I also added two more tests to make sure the program throws the right error if the debit amount is less than 0 or more than the current balance. I used the Assert.ThrowsException method to test these errors.

This small project showed me how useful unit tests are. They can catch mistakes early and help me improve my code. I now feel more confident about writing and using unit tests in my own projects.
