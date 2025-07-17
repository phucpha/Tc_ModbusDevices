(*Ch?c ch?n r?ng m?i test case ki?m th? m?c ??n v? s? ??c l?p v?i nh?ng test case kh�c.
 Kh�ng n�n g?i m?t test case kh�c trong m?t test case. Test case kh�ng n�n ph? thu?c v�o nhau c? v? data v� th? t? th?c hi?n.
Lu�n lu�n ki?m tra t?ng m�-?un m?t c�ch ??c l?p. 
N?u kh�ng, s? c� nhi?u s? ch?ng ch�o gi?a c�c ca th? nghi?m v� vi?c thay ??i ??i v?i m?t ??n v? c� th? ?nh h??ng ??n t?t c? c�c m�-?un
 kh�c v� khi?n ph?n m?m b? l?i.
??t t�n c�c ??n v? ki?m th? m?t c�ch r� r�ng v� nh?t qu�n. 
??m b?o r?ng c�c test case d? ??c, b?t k? ai c?ng c� th? ch?n test case v� ch?y n� m� kh�ng g?p b?t k? v?n ?? n�o.
Khi tri?n khai vi?c thay ??i giao di?n ho?c ch?c n?ng, 
c?n ch?y l?i c�c test case tr??c ?� nh?m ??m b?o vi?c thay ??i n�y kh�ng l�m ?nh h??ng ??n nh?ng test case c? ?� pass.
Lu�n ??m b?o l?i ???c x�c ??nh trong qu� tr�nh Unit test ???c s?a tr??c khi chuy?n sang giai ?o?n ti?p theo.
Kh�ng c? g?ng vi?t test case ?? ki?m th? t?t c? m?i th?, thay v�o ?� n�n t?p chung v�o ki?m th? s? ?nh h??ng c?a h�nh vi h? th?ng
B�n c?nh vi?t test case ?? test h�nh vi h? th?ng, c?n vi?t th�m test case ?? ki?m th? hi?u n?ng c?a m� ngu?n
C�c testsuit n�n ??t ri�ng ra, ??c l?p code v?i module
Kh�ng n�n c� nhi?u assert trong m?t test case v� khi m?t ?i?u ki?n kh�ng th?a m�n th� c�c assert kh�c s? b? b? qua
Sau m?t th?i gian d�i, s? l??ng test case nhi?u, th?i gian ch?y l?n.
 N�n chia ra nh�m test case c? v� test case m?i, test case c? s? ch?y v?i t?n xu?t �t h?n*)
 
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
 