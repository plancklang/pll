# PLL (Planck Lang Library)
Plank Lang Standard Library

- io.plk
- list.plk
- math.plk
- struct.plk

```c
~/
~ This file contains functions that help with mathematical operations
~
~ Jake Roggenbuck (jakeroggenbuck2@gmail.com)
/~

double pi = 3.141592653589793238462643383279502884197;
double e = 2.718281828459045235360287471352662497757;


total(nums: list): int {
	~ Get mean of list ~
	if (nums.length != 0) {
		int total_of_nums = 0;
		loop (nums) : int num {
			total_of_nums += num;
		}
		return total_of_nums;
	} else {
		return 0;
	}
}

mean(nums: list): int {
	~ Get mean of list ~
	return 0 if (nums.length == 0) else total(nums) / nums.length;
}

factorial(num: int): int {
	~ Get factorial of number ~
	if (num < 0) {
		return 0;
	} elif (num == 0 or num == 1) {
		return 1;
	} else {
		int fact = 1;
		while (num > 1) {
			fact *= num;
			num--;
		}
		return fact;
	}
}

is_finite(num: double): bool {
	~ Returns true if num is finite ~
}

is_null(num: double): bool {
	~ Returns if num is null ~
	if (num == none) {
		return true;
	}
}

exp(base_num: double, exponent_num: double): double {
	double num = base_num;
	~ Is either num not finite ~
	if (!is_finite(base_num) || !is_finite(exponent_num)) {
		~ One of the nums is not finite, so more work needs to be done ~
	} else
	    loop (exponent_num - 1): {
			num *= base_num;
		}
		return num;
	}
}
```
