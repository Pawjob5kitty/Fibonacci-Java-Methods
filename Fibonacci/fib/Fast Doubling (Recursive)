
public static long[] fibFastDoubling(long n) {
    if (n == 0) return new long[]{0, 1};

    long[] half = fibFastDoubling(n / 2);
    long f_k = half[0];
    long f_k_plus_1 = half[1];

    long f_2k = f_k * (2 * f_k_plus_1 - f_k);
    long f_2k_plus_1 = f_k * f_k + f_k_plus_1 * f_k_plus_1;

    if (n % 2 == 0) return new long[]{f_2k, f_2k_plus_1};
    else return new long[]{f_2k_plus_1, f_2k + f_2k_plus_1};
}
