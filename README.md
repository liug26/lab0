# A Kernel Seedling
For this lab, I made a kernel module, which counts the number of currently running processes.

## Building
```shell
To compile and build the kernel module, run `make`. 
```

## Running
```shell
Run the following commands after make:
sudo insmod proc_count.ko
cat /proc/count
this should output the number of currently running processes.
For me, it outputs 88
```

## Cleaning Up
```shell
Run the following command to remove the kernel module:
sudo rmmod proc_count
```

## Testing
```python
python -m unittest
```
Results: Passed all 3 tests.

Report which kernel release version you tested your module on
(hint: use `uname`, check for options with `man uname`).
It should match release numbers as seen on https://www.kernel.org/.

```shell
uname -r -s -v
```

My kernel version is: Linux 5.14.8-arch1-1
