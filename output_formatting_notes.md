setw: adds spaces to get the next output up to the minimum number of characters entered. If the next output is already greater than or equal to that, then it does nothing.
example: 
  cout << '*' << "setw 10" << endl;
  cout << '*' << setw(10) << 2 << '*'<< endl;
output: 
  *setw 10
  *         2*


justification: may use left, right, or internal to tell it where to put the padding for setw. left puts the padding to the right of the next output, internal puts the side/prefix to the left, padding in the middle, and value to the right. Right puts padding to the left of the next output. once you set, them, they remain until you change the setting. The default is right.

example:
  cout << right;
  cout << "*" << setw(6) << -23 << "*" << endl;
output:
  *   -23*

boolalpha: can display boolean values as true or false. to undo it, enter noboolalpha instead.

example:
  bool a = true, b = false;

  cout << "a " << a << endl;
  cout << boolalpha <<  "a " << a << endl;
output:
  a 1
  a true

displaying decimal, octal, and hexadecimal using hex, dec, and oct. showbase may show a base of nothing, 0, or 0x

example:
  cout << "With showbase" << endl;
  cout << showbase;
  cout << "a (decimal) " << dec << a << endl;
  cout << "a (octal) " << oct << a << endl;
  cout << "a (hex) " << hex << a << endl;

  cout << "With noshowbase" << endl;
  cout << noshowbase;
  cout << "a (decimal) " << dec << a << endl;
  cout << "a (octal) " << oct << a << endl;
  cout << "a (hex) " << hex << a << endl;
output: 
  With showbase
  a (decimal) 234532
  a (octal) 0712044
  a (hex) 0x39424
  With noshowbase
  a (decimal) 234532
  a (octal) 712044
  a (hex) 39424

uppercase and nouppercase: these will change how hexadecimal numbers are displayed and the e in scientific notation to upper or lower case.

showpos and noshowpos: Use showpos and noshowpos to print + next to a positive number.

setfill: changes padding for setw
example:
    cout << "setfill('*'): " << setfill('*');

Displaying floating point numbers:
For overall display, C++ finds the more pleasant option between fixed and scientific format. once you specify, it is difficult to revert to general choice.
setprecision is used to specify roughly the number of digits displayed for the number. In general format, the setprecision specifies the maximum number of digits displayed. This includes digits before and after the decimal point, excluding the decimal point. In fixed and scientific formats, the precision specifies the number of digits after the decimal point.
showpoint modifier can be used to display the trailing zeros.
