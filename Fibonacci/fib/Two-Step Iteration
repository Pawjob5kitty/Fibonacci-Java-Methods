
public static long fibTwoStep(int n) {
    long f1 = 0;
    long f2 = 1;

    for (int i = 0; i < n / 2; i++) {
        long temp1 = f1 + f2;
        long temp2 = f2 + temp1;
        f1 = temp1;
        f2 = temp2;
    }

    if (n % 2 == 0) return f1;
    else return f2;
}
