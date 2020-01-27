# Please help me with this code Project-Euler: Problem 47 - Distinct primes factors 

I need someone to explain to me how this code works. It is written in Visual Basic in Excel (IT MUST BE WRITTEN IN VISUAL BASIC IN EXCEL, it is for my university).
My friends did it for me, but I don't understand it and it is really urgent. 
Thank you in advance. 

-----------------------------------------------------------------------------
# The problem goes: 
How do I find 4 sequential 4-digit numbers that contain 4 prime number multiples (that make up the 4-digit number when multiplied, the multiples don't have to be the same) in Visual Basic?

The first two consecutive numbers to have two distinct prime factors are:

14 = 2 × 7
15 = 3 × 5

The first three consecutive numbers to have three distinct prime factors are:

644 = 2² × 7 × 23
645 = 3 × 5 × 43
646 = 2 × 17 × 19.

Find the first four consecutive integers to have four distinct prime factors each. What is the first of these numbers?

-----------------------------------------------------------------------------
You can see my code down below, if you do not want to download it from GitHub:

`Sub main()

Dim nadjen As Boolean 

Dim b As Long 

nadjen = False

b = 1

 While Not nadjen

 If (primovi(b) = 4) Then

b = b + 1

 If (primovi(b) = 4) Then 

b = b + 1 

If (primovi(b) = 4) Then 

b = b + 1 

If (primovi(b) = 4) Then 

nadjen = True 

End If 

End If 

End If 

End If 

b = b + 1 

Wend 

MsgBox (b - 4 & ", " & b - 3 & ", " & b - 2 & ", " & b - 1)

End Sub


Function primovi(ByVal x As Long) As Integer

Dim a As Integer 

Dim i As Long 

i = 2

While (x <> 1 Or x > i) 

If ((x Mod i) = 0) Then 

x = x / i 

a = a + 1 

i = i - 1 

End If 

i = i + 1 

Wend 

primovi = a

End Function
