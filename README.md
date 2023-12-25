# Reach-Target-in-Minimum-Steps
#include <iostream>

int minStepsToTarget(int target) {
    int steps = 0;
    while (target > 0) {
        if (target % 2 == 0) {
            target /= 2;
        } else {
            target -= 1;
        }
        steps += 1;
    }
    return steps;
}

int main() {
    int target;
    std::cin >> target;

    int result = minStepsToTarget(target);
    std::cout << result << std::endl;

    return 0;
}
