(*Ch?c ch?n r?ng m?i test case ki?m th? m?c ??n v? s? ??c l?p v?i nh?ng test case khác.
 Không nên g?i m?t test case khác trong m?t test case. Test case không nên ph? thu?c vào nhau c? v? data và th? t? th?c hi?n.
Luôn luôn ki?m tra t?ng mô-?un m?t cách ??c l?p. 
N?u không, s? có nhi?u s? ch?ng chéo gi?a các ca th? nghi?m và vi?c thay ??i ??i v?i m?t ??n v? có th? ?nh h??ng ??n t?t c? các mô-?un
 khác và khi?n ph?n m?m b? l?i.
??t tên các ??n v? ki?m th? m?t cách rõ ràng và nh?t quán. 
??m b?o r?ng các test case d? ??c, b?t k? ai c?ng có th? ch?n test case và ch?y nó mà không g?p b?t k? v?n ?? nào.
Khi tri?n khai vi?c thay ??i giao di?n ho?c ch?c n?ng, 
c?n ch?y l?i các test case tr??c ?ó nh?m ??m b?o vi?c thay ??i này không làm ?nh h??ng ??n nh?ng test case c? ?ã pass.
Luôn ??m b?o l?i ???c xác ??nh trong quá trình Unit test ???c s?a tr??c khi chuy?n sang giai ?o?n ti?p theo.
Không c? g?ng vi?t test case ?? ki?m th? t?t c? m?i th?, thay vào ?ó nên t?p chung vào ki?m th? s? ?nh h??ng c?a hành vi h? th?ng
Bên c?nh vi?t test case ?? test hành vi h? th?ng, c?n vi?t thêm test case ?? ki?m th? hi?u n?ng c?a mã ngu?n
Các testsuit nên ??t riêng ra, ??c l?p code v?i module
Không nên có nhi?u assert trong m?t test case vì khi m?t ?i?u ki?n không th?a mãn thì các assert khác s? b? b? qua
Sau m?t th?i gian dài, s? l??ng test case nhi?u, th?i gian ch?y l?n.
 Nên chia ra nhóm test case c? và test case m?i, test case c? s? ch?y v?i t?n xu?t ít h?n*)
 
(*Perspective:
So let's take a step back and ask what TDD is trying to help us with.
 TDD is trying to help us determine if our code is correct or not. And by correct,
 I mean "does the code meet the business requirements?" The selling point is that we know changes will be required in the future, 
and we want to make sure that our code remains correct after we make those changes.

I bring that perspective up because I think it's easy to get lost in the details and lose sight of what we're trying to achieve.

Principles - SAP:
While I'm not an expert in TDD, I think you're missing part of what Single Assertion Principle (SAP) is trying to teach.
 SAP can be restated as "test one thing at a time." But TOTAT doesn't roll off the tongue as easily as SAP does.

Testing one thing at a time means that you focus on one case; one path; one boundary condition; 
one error case; one whatever per test. 
And the driving idea behind that is you need to know what broke when the test case fails, so you can resolve the issue more quickly. 
If you test multiple conditions (ie. more than one thing) within a test and the test fails,
 then you have a lot more work on your hands. 
You first have to identify which of the multiple cases failed and then figure out why that case failed.
If you test one thing at a time, your search scope is a lot smaller and the defect is identified more quickly.
 Keep in mind that "test one thing at a time" doesn't necessarily exclude you from looking at more than one
 process output at a time. For example, when testing a "known good path", I may expect to see a specific,
 resulting value in foo as well as another value in bar and I may verify that foo != bar as part of my test. 
The key is to logically group the output checks based upon the case being tested.
Principles - PMP:
Likewise, I think you're missing a bit about what Private Method Principle (PMP) has to teach us. 
PMP encourages us to treat the system like a black box. For a given input, you should get a given output. 
You don't care how the black box generates the output. You only care that your outputs align with your inputs.

PMP is really good perspective for looking at the API aspects of your code. 
It can also help you scope what you have to test. 
Identify your interface points and verify that they meet the terms of their contracts. 
You don't need to care about how the behind-the-interface (aka private) methods do their job. 
You just need to verify they did what they were supposed to do.*) 
 