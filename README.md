# Impedance-Matrix-Creation
The code aims to create an impedance matrix in a Power System based on user input. The user specifies the number of elements, and then for each pair of elements, the code prompts the user to enter the impedance value between them.

Here is the code:


clc;
clear all;
close all;
n = input('enter the no of elements:');
%%z=complex(0,0);
    for q=1:n
        for r= 1:n
            fprintf('Enter the impedance value between %d-%d', q,r);
            z(q,r)=input(':');
   
             if(q~=r)
                  zb(q,r)=-1*(z(q,r))
             else
                 zb(q,r)=(z(q,r))
            end
   
        end
    end
    
    
    
clc;, clear all;, close all;: These commands clear the command window, workspace variables, and close any open figures, respectively. They ensure a clean workspace before running the code.

n = input('enter the no of elements:');: This line prompts the user to enter the number of elements and assigns the input value to the variable n.

for q=1:n: This is a for loop that iterates from 1 to the value of n. It represents the index of the first element.

for r=1:n: This is another nested for loop that iterates from 1 to the value of n. It represents the index of the second element.

fprintf('Enter the impedance value between %d-%d', q, r);: This line prints the message "Enter the impedance value between x-y" to the command window, where x and y are the values of q and r, respectively.

z(q,r) = input(':');: This line prompts the user to enter the impedance value between the q-th and r-th elements and assigns the input value to the matrix element z(q,r).

if (q ~= r): This is an if statement that checks if the indices q and r are not equal.

zb(q,r) = -1 * (z(q,r)): If the indices q and r are not equal, it assigns the negative value of z(q,r) to the matrix element zb(q,r).

else: If the indices q and r are equal.

zb(q,r) = z(q,r): It assigns the value of z(q,r) to the matrix element zb(q,r).

The code aims to create an impedance matrix based on user input. The user specifies the number of elements, and then for each pair of elements, the code prompts the user to enter the impedance value between them. If the indices of the elements are not equal, the corresponding element in the impedance matrix zb is assigned the negative value of the impedance. If the indices are equal, the impedance value is assigned directly to the matrix.
