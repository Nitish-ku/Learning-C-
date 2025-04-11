#include <cs50.h>
#include <stdio.h>
int quarter(int a);
int dime(int b);
int nickel(int c);
int penny(int d);

int main(void)
{
    int change;
    int coins;
    do
    {
        change = get_int("Change owed: ");
    }
    while (change < 1);

    int quarter_coin = quarter(change);
    change = change - (25 * quarter_coin);

    int dime_coin = dime(change);
    change = change - (10 * dime_coin);

    int nickel_coin = nickel(change);
    change = change - (5 * nickel_coin);

    int penny_coin = penny(change);
    change = change - (1 * penny_coin);

    coins = quarter_coin + dime_coin + nickel_coin + penny_coin;

    printf("%i\n", coins);
}

int quarter(int a)
{
    return a / 25;
}

int dime(int b)
{
    return b / 10;
}

int nickel(int c)
{
    return c / 5;
}

int penny(int d)
{
    return d / 1;
}
