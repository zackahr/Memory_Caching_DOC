```#include <iostream>
#include <chrono>

// Function to calculate Fibonacci number recursively
int fibonacci(int n) {
    if (n <= 1) {
        return n;
    } else {
        return fibonacci(n - 1) + fibonacci(n - 2);
    }
}

int main() {
    int n;
    std::cout << "Enter the number of terms you want in Fibonacci series: ";
    std::cin >> n;

    std::chrono::steady_clock::time_point start = std::chrono::steady_clock::now();

    std::cout << "Fibonacci Series:\n";
    for (int i = 0; i < n; ++i) {
        std::cout << fibonacci(i) << " ";
    }
    std::cout << std::endl;

    std::chrono::steady_clock::time_point end = std::chrono::steady_clock::now();
    std::chrono::duration<double> duration = std::chrono::duration_cast<std::chrono::duration<double>>(end - start);

    std::cout << "Execution time: " << duration.count() << " seconds" << std::endl;

    return 0;
}
```

for example if we toke the normal algorithm of the Fibonacci we would found that for example the number 45 it will take about 20s too execute.