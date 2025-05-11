# Text Processing program
clear all ;
my_text = fileread('file path');
my_text = string(my_text);
disp("Original Text including empty lines")
my_text = splitlines(my_text)

TF = (my_text == ""); % create logical array for indices with empty lines;
disp("Text without empty lines")
my_text(TF) = [] % i think make the lines of indices of my_text which equals to zero  empty

p = {'.', '?', '!', ','}; % p is a varib type cell ,  cell is a special type of variable that can hold different types and sizes of data in the same container

disp("Text without empty lines and punctiuations")

my_text = replace(my_text,p, ' ') % replace the characters in my_text in p  with emptay space

disp("Text without header and end spaces")

my_text = strip(my_text) % remove the spaces before and after

disp("statistics on my_text")
my_text = join(my_text); % join  all text lines into one entitiy
my_text = split(my_text); % split each word at delimiters

tabulate(my_text) %to show statistics and 
