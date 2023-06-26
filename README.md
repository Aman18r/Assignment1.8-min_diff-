# Assignment1.8-min_diff-

import java.util.*;

class Main {

    static int minDiff(int arr[], int n, int k) {
        int result = Integer.MAX_VALUE;


        Arrays.sort(arr);


        for (int i = 0; i <= n - k; i++)
            result = Math.min(result, arr[i + k - 1] - arr[i]);

        return result;
    }


    public static void main(String[] args) {
        int arr[] = {1};
        int n = arr.length;
        int k = 3;

        System.out.println(minDiff(arr, n, k));
    }
}
