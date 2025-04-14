using debug50 in the terminal 

#include <stdio.h>
#include <cs50.h>

void print_column(int height);

int main(void)
{
    int h = get_int("height: ");
    print_column(h);
}

void print_column(int height)
{
    for (int i = 0; i<=height; i++)
    {
        printf("#\n");
    }
}





$ cd '/workspaces/169964150/practice'
practice/ $ make hello
practice/ $ ./hello
height: 4
#
#
#
#
#
practice/ $ debug50 ./hello
Looks like you haven't set any breakpoints. Set at least one breakpoint by clicking to the left of a line number and then re-run debug50!
practice/ $ debug50 ./hello
Unable to launch debugger.
practice/ $ debug50 ./hello
practice/ $ debug50 ./hello
practice/ $ ^C
