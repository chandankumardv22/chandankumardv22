import java.util.*;
public class Quick {
    static int count = 0;
    static void mergesort(int[] a) {
        int n = a.length;
        if (n > 1) {
            int pSize = (int) Math.floor(n / 2.0);
            int qSize = (int) Math.ceil(n / 2.0);
            int[] p = new int[pSize];
            int[] q = new int[qSize];
            System.arraycopy(a, 0, p, 0, pSize);
            System.arraycopy(a, pSize, q, 0, qSize);
            mergesort(p);
            mergesort(q);
            merge(a, p, q);
        }
    }
    static void merge(int[] a, int[] p, int[] q) {
        int i = 0, j = 0, k = 0;
        int pLen = p.length;
        int qLen = q.length;
        while(i < pLen && j < qLen) {
            count++;
            if (p[i] <= q[j]) {
                a[k++] = p[i++];
            } else {
                a[k++] = q[j++];
            }
        }
        while (i < pLen) {
            a[k++] = p[i++];
        }
        while (j < qLen) {
            a[k++] = q[j++];
        }
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of elements:");
        int n = sc.nextInt();
        int[] a = new int[n];
        Random rand = new Random();
        System.out.println("Input array (random numbers):");
        for (int i = 0; i < n; i++) {
            a[i] = rand.nextInt(1000);
            System.out.print(a[i] + " ");
        }
        System.out.println();
        mergesort(a);
        System.out.println("Sorted array:");
        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }
        System.out.println();
        System.out.println("Number of basic operations: " + count);
        System.out.println("Best case (Lower bound): " + (int) (n * Math.log(n) / Math.log(2)));
        System.out.println("Worst case: " + (int) (n * Math.log(n) / Math.log(2)));
    }
}
