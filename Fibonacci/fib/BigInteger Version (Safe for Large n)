
import java.math.BigInteger;

public static BigInteger fibBig(int n) {
    BigInteger prev = BigInteger.ZERO;
    BigInteger current = BigInteger.ONE;

    for (int i = 0; i < n; i++) {
        BigInteger next = prev.add(current);
        prev = current;
        current = next;
    }

    return prev;
