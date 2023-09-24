#include <stdio.h>
#include <math.h>
#define pi_d 180
int basicmaths();
int trigonometric();
int logln();
int quadratic();
int determinent();
int table();
int expo();
int fact();
int sumupton();
int unitconversion();
int main()
{
    int fun, again;
    printf("The Precision Value of Calculator is 3\n");
    do
    {
        printf("Press\n1 for Basic Calculation(+, -, *, /, %c)\n2 for Trigonometric Function(sin,cos,tan,cot,sec,coses and it's inverse)\n3 for log & ln\n4 for Exponential\n5 for determinent\n6 for solution of Quadratic Equation\n7 for Multiplication Table\n8 for Factorial\n9 for sum of all Natural Number up to n with any power\n10 for Unit Conversion\n", 37);
        scanf("%d", &fun);
        switch (fun)
        {
        case 1:
            basicmaths();
            break;
        case 2:
            trigonometric();
            break;
        case 3:
            logln();
            break;
        case 4:
            expo();
            break;
        case 5:
            determinent();
            break;
        case 6:
            quadratic();
            break;
        case 7:
            table();
            break;
        case 8:
            fact();
            break;
        case 9:
            sumupton();
            break;
        case 10:
            unitconversion();
            break;
        }
        printf("\n\nPress 0 to exit or 1 to continue: ");
        scanf("%d", &again);
    } while (again != 0);
    return 0;
}
int basicmaths()
{
    // Scanning The Numbers
    float a, b;
    printf("1st Number a = ");
    scanf("%f", &a);
    printf("2nd Number b = ");
    scanf("%f", &b);
    // Operator
    printf("\nPress 1 for a+b\n");
    printf("Press 2 for a-b\n");
    printf("Press 3 for b-a\n");
    printf("Press 4 for a*b\n");
    printf("Press 5 for a/b\n");
    printf("Press 6 for b/a\n");
    printf("Press 7 for a%cb\n", 37);
    printf("Press 8 for b%ca\n", 37);
    int operate;
    scanf("%d", &operate);
    printf("You have chose this number of Operator : %d\n", operate);
    // if and else condition
    switch (operate)
    {
    case 1:
        printf("\na + b = %.3f", a + b);
        break;
    case 2:
        printf("\na - b = %.3f", a - b);
        break;
    case 3:
        printf("\nb - a = %.3f", b - a);
        break;
    case 4:
        printf("\na*b = %.3f", (float)a * b);
        break;
    case 5:
        printf("\na/b = %.3f", (float)a / b);
        break;
    case 6:
        printf("\nb/a = %.3f", (float)b / a);
        break;
    case 7:
        printf("\na%cb = %d", 37, (int)a % (int)b);
        break;
    case 8:
        printf("\na%cb = %d", 37, (int)b % (int)a);
        break;
    default:
        printf("\nYou Should make a habit of Listening to the Instructions");
        break;
    }
    return 0;
}
int trigonometric()
{
    char trig_fun, val;
    int que;
    float ang;
    printf("(Trigonometric Function / Inverse Trigonometric Function) : (Y / N)\n");
    scanf("%s", &trig_fun);
    if (trig_fun == 'Y' || trig_fun == 'y')
    {
        printf("(Angle in Radian / Angel in Degree) : (Y / N)");
        val = getchar();
        if (val == 'y' || val == 'Y')
        {
            int x, y;
            printf("x*%c/y\nwrite the value of x and y\n", 227);
            printf("x = ");
            scanf("%d", &x);
            printf("y = ");
            scanf("%d", &y);
            ang = (x * pi_d) / y;
        }
        else
        {
            printf("Write the angle you want to find the Trigonomic Function of : ");
            scanf("%f", &ang);
        }
        printf("Press 1 for sin\n2 for cos\n3 for tan\n4 for cot\n5 for sec\n6 for cosec\n");
        scanf("%d", &que);
        switch (que)
        {
        case 1:
            printf("sin(%f) = ", sin(ang));
            break;
        case 2:
            printf("cos(%f) = ", cos(ang));
            break;
        case 3:
            printf("tan(%f) = ", tan(ang));
            break;
        case 4:
            printf("cot(%f) = ", 1 / tan(ang));
            break;
        case 5:
            printf("sec(%f) = ", 1 / cos(ang));
            break;
        case 6:
            printf("coses(%f) = ", 1 / sin(ang));
            break;
        default:
            printf("\nYou Should make a habit of Listening to the Instructions");
            break;
        }
    }
    else
    {
        float ans;
        printf("Write the value you want to find the Inverse of : ");
        scanf("%f", &ang);
        printf("Press 1 for sin-1\n2 for cos-1\n3 for tan-1\n");
        scanf("%d", &que);
        switch (que)
        {
        case 1:
            ans = asin(ang);
            printf("sin^-1(%.3f) = %.3f*%c", ang, ans / 3.14, 227);
            break;
        case 2:
            ans = acos(ang);
            printf("cos^-1(%.3f) = %.3f*%c", ang, ans / 3.14, 227);
            break;
        case 3:
            ans = atan(ang);
            printf("tan^-1(%.3f) = %.3f*%c", ang, ans / 3.14, 227);
            break;
        default:
            printf("\nYou Should make a habit of Listening to the Instructions");
            break;
        }
    }
    return 0;
}
int logln()
{
    int log_ln;
    printf("Press 1 if your Log base is e = 2.718\nPress anything else if your Log base is anything other than e\n");
    scanf("%d", &log_ln);
    if (log_ln == 1)
    {
        float val, y;
        printf("Type the Value of which you want to find ln of : ");
        scanf("%f", &y);
        val = log(y);
        printf("\nln(%f) = %.3f", y, val);
    }
    else
    {
        float x1, x2, ans, y1, y2;
        printf("Type the Value of log : ");
        scanf("%f", &x1);
        printf("Type the Base of log : ");
        scanf("%f", &x2);
        // value
        y1 = log(x1);
        // Base
        y2 = log(x2);
        // answer
        ans = y1 / y2;
        printf("log\t%.3f = %.3f\n", x1, ans);
        printf("   %.3f", x2);
    }
    return 0;
}
int quadratic()
{
    float Root1, Root2, d;
    int a, b, c;
    printf("ax%c+bx+c\nEnter The Values of a, b, c to find x with precision value of 3\n", 253);
    scanf("%d %d %d", &a, &b, &c);
    d = (b * b) - (4 * a * c);
    switch (d > 0)
    {
    case 1:
        Root1 = ((-b) + sqrt(d)) / (2 * a);
        Root2 = ((-b) - sqrt(d)) / (2 * a);
        printf("Sr.no\tInputs \tRoot1\tRoot2\timanginary\n");
        printf(" \ta b c \n");
        printf("1.   \t%d %d %d\t%.3f\t%.3f\t", a, b, c, Root1, Root2);
        break;
    case 0:
        switch (d < 0)
        {
        case 1:
            printf("The Answer is Imaginary\n");
            Root1 = -b / (2 * a);       // ans 1 is real part
            Root2 = sqrt(-d) / (2 * a); // ans 2 is imaginary part
            printf("Sr.no\tInputs \tRoot1\tRoot2\timanginary\n");
            printf(" \ta b c \n");
            printf("1.   \t%d %d %d\t%.3f\t\t%.3f i", a, b, c, Root1, Root2);
            break;
        case 0:
            Root1 = -b / (2 * a); // Root1 and ans 2 are the same
            printf("Sr.no\tInputs\tRoot1\tRoot2\timanginary\n");
            printf(" \ta b c \n");
            printf("1.   \t%d %d %d\t%.3f", a, b, c, Root1);
            break;
        }
        break;
    }
    return 0;
}
int determinent()
{
    printf("You can only find determinent of Matrix order 5X5, 4X4, 3X3, 2X2 with the use of this Programme\n");
    int order;
    float A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, V, W, X, Y, Z, a, b, c, d, e, f, g, h, i, Det;
    printf("Enter the order of the Determinent : ");
    scanf("%d", &order);
    switch (order)
    {
    case 2:
        // Getting The Values
        printf("A\tB\n\nC\tD\n");
        printf("A = ");
        scanf("%f", &A);
        printf("B = ");
        scanf("%f", &B);
        printf("C = ");
        scanf("%f", &C);
        printf("D = ");
        scanf("%f", &D);
        // Calculations
        Det = (A * D) - (B * C);
        printf("The Answer of the Determinent of order %d = %.3f", order, Det);
        break;
    case 3:
        // getting the values
        printf("A\tB\tC\n\nD\tE\tF\n\nG\tH\tI\n");
        printf("A = ");
        scanf("%f", &A);
        printf("B = ");
        scanf("%f", &B);
        printf("C = ");
        scanf("%f", &C);
        printf("D = ");
        scanf("%f", &D);
        printf("E = ");
        scanf("%f", &E);
        printf("F = ");
        scanf("%f", &F);
        printf("G = ");
        scanf("%f", &G);
        printf("H = ");
        scanf("%f", &H);
        printf("I = ");
        scanf("%f", &I);
        // Calculation
        Det = A * ((E * I) - (H * F)) - B * ((D * I) - (G * F)) + C * ((D * H) - (G * E));
        printf("The Answer of the Determinent of order %d = %.3f", order, Det);
        break;
    case 4:
        // Getting the Values
        printf("A\tB\tC\tD\n\nE\tF\tG\tH\n\nI\tJ\tK\tL\n\nM\tN\tO\tP\n");
        printf("A = ");
        scanf("%f", &A);
        printf("B = ");
        scanf("%f", &B);
        printf("C = ");
        scanf("%f", &C);
        printf("D = ");
        scanf("%f", &D);
        printf("E = ");
        scanf("%f", &E);
        printf("F = ");
        scanf("%f", &F);
        printf("G = ");
        scanf("%f", &G);
        printf("H = ");
        scanf("%f", &H);
        printf("I = ");
        scanf("%f", &I);
        printf("J = ");
        scanf("%f", &J);
        printf("K = ");
        scanf("%f", &K);
        printf("L = ");
        scanf("%f", &L);
        printf("M = ");
        scanf("%f", &M);
        printf("N = ");
        scanf("%f", &N);
        printf("O = ");
        scanf("%f", &O);
        printf("P = ");
        scanf("%f", &P);
        // Calculations
        W = A * (F * ((K * P) - (L * O)) - G * ((J * P) - (L * N)) + H * ((J * O) - (K * N)));
        X = B * (E * ((K * P) - (L * O)) - G * ((I * P) - (M * L)) + H * ((I * O) - (K * M)));
        Y = C * (E * ((J * P) - (L * N)) - F * ((I * P) - (L * M)) + H * ((I * N) - (J * M)));
        Z = D * (E * ((J * O) - (K * N)) - F * ((I * O) - (K * M)) + G * ((I * N) - (J * M)));
        Det = W - X + Y - Z;
        printf("The Answer of the Determinent of order %d = %.3f", order, Det);
        break;
    case 5:
        // Getting the Values
        printf("A\tB\tC\tD\tE\n\nF\tG\tH\tI\tJ\n\nK\tL\tM\tN\tO\n\nP\tQ\tR\tS\tT\n\nU\tV\tW\tX\tY\n");
        printf("A = ");
        scanf("%f", &A);
        printf("B = ");
        scanf("%f", &B);
        printf("C = ");
        scanf("%f", &C);
        printf("D = ");
        scanf("%f", &D);
        printf("E = ");
        scanf("%f", &E);
        printf("F = ");
        scanf("%f", &F);
        printf("G = ");
        scanf("%f", &G);
        printf("H = ");
        scanf("%f", &H);
        printf("I = ");
        scanf("%f", &I);
        printf("J = ");
        scanf("%f", &J);
        printf("K = ");
        scanf("%f", &K);
        printf("L = ");
        scanf("%f", &L);
        printf("M = ");
        scanf("%f", &M);
        printf("N = ");
        scanf("%f", &N);
        printf("O = ");
        scanf("%f", &O);
        printf("P = ");
        scanf("%f", &P);
        printf("Q = ");
        scanf("%f", &a);
        printf("R = ");
        scanf("%f", &b);
        printf("S = ");
        scanf("%f", &c);
        printf("T = ");
        scanf("%f", &d);
        printf("U = ");
        scanf("%f", &e);
        printf("V = ");
        scanf("%f", &f);
        printf("W = ");
        scanf("%f", &g);
        printf("X = ");
        scanf("%f", &h);
        printf("Y = ");
        scanf("%f", &i);
        // calculation
        V = A * (G * (L * (c * i - h * d) - M * (b * i - g * d) + N * (b * h - c * g)) - H * (K * (c * i - h * d) - M * (a * i - f * d) + N * (a * h - f * d)) + I * (K * (b * i - g * d) - L * (a * i - f * d) + N * (a * g - f * b)) - J * (K * (b * h - g * e) - L * (a * h - f * e) + M * (a * g - f * b)));
        W = B * (F * (M * (C * i - d * h) - N * (b * i - g * d) + O * (b * h - g * c)) - H * (K * (c * i - h * d) - N * (P * i - e * d) + O * (P * h - e * c)) + I * (K * (b * i - g * d)));
        Det = V - W;
        printf("The Answer of the Determinent of order %d = %.3f", order, Det);
    default:
        printf("You should listen to the Instructions");
        break;
    }

    return 0;
}
int table()
{
    int a, m;
    printf("Enter the Number : ");
    scanf("%d", &a);
    for (m = 1; m < 11; m++)
    {
        printf("%d * %d = %d\n", a, m, a * m);
    }
    return 0;
}
int expo()
{
    float base, power, ans;
    int e;
    printf("Type 1 if the base is e or anything else for another number");
    scanf("%d", &e);
    if (e == 1)
    {
        printf("Enter the power of the Exponential Function : ");
        scanf("%f", &power);
        ans = exp(power);
        printf("e^%.3f = %.3f", power, ans);
    }
    else
    {
        printf("Enter the Base of the Exponential Function : ");
        scanf("%f", &base);
        printf("Enter the Power of the Exponential Function : ");
        scanf("%f", &power);
        ans = pow(base, power);
        printf("%.3f^%.3f = %.3f", base, power, ans);
    }
    return 0;
}
int fact()
{
    int m, b;
    float a;
    printf("Enter the Number : ");
    scanf("%f", &a);
    b = a;
    for (m = 1; m < 11; m++)
    {
        a = a * m;
    }
    printf("%d! = %.3f", b, a);
    return 0;
}
int sumupton()
{
    int i, n, power;
    double ans = 0;
    printf("Enter the value of n : ");
    scanf("%d", &n);
    printf("Enter the Power : ");
    scanf("%d", &power);
    for (i = 1; i <= n; i++)
    {
        ans = ans + pow(i, power);
    }
    printf("The sum of all numbers upto %d with power %d is %.0lf", n, power, ans);
    return 0;
}
int unitconversion()
{
    int unit, temp, length, weight;
    double in, out;
    printf("Press\n1 for Temprature\n2 for length\n3 for weight\n");
    scanf("%d", &unit);
    switch (unit)
    {
    case 1:
        printf("Press\n1 for Celcius to Farenhite\n2 for Farenhite to Celcius\n");
        scanf("%d", &temp);
        switch (temp)
        {
        case 1:
            printf("Enter the temprature in Celcius : ");
            scanf("%lf", &in);
            out = (9 / 5) * in + 32;
            printf("%.3lf degree Celcius = %.3lf Farenhite", in, out);
            break;
        case 2:
            printf("Enter the temprature in Farenhite : ");
            scanf("%lf", &in);
            out = (in - 32) * (5 / 9);
            printf("%.3lf Farenhite = %.3lf Degree Celcius", in, out);
            break;
        }
        break;
    case 2:
        printf("Press\n1 for centimeter to meter\n2 for meter to centimeter\n3 for meter to kilometer\n4 for kilometer to meter\n5 for centimeter to kilometer\n6 for kilometer to centimeter");
        scanf("%d", &length);
        switch (length)
        {
        case 1:
            printf("Enter the length in centimeter : ");
            scanf("%lf", &in);
            out = in / 100;
            printf("%.3lf centimeter = %lf meter", in, out);
            break;
        case 2:
            printf("Enter the length in meter : ");
            scanf("%lf", &in);
            out = in * 100;
            printf("%.3lf meter = %.3lf centimeter", in, out);
            break;
        case 3:
            printf("Enter the length in meter : ");
            scanf("%lf", &in);
            out = in / 1000;
            printf("%.3lf meter = %lf kilometer", in, out);
            break;
        case 4:
            printf("Enter the length in kilometer : ");
            scanf("%lf", &in);
            out = in * 1000;
            printf("%.3lf kilometer = %.3lf meter", in, out);
            break;
        case 5:
            printf("Enter the length in centimeter : ");
            scanf("%lf", &in);
            out = in / 100000;
            printf("%.3lf centimeter = %lf kilometer", in, out);
            break;
        case 6:
            printf("Enter the length in kilometer : ");
            scanf("%lf", &in);
            out = in * 100000;
            printf("%.3lf kilometer = %.3lf centimeter", in, out);
            break;
        }
        break;
    case 3:
        break;
    }
    return 0;
}