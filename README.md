# QCOM_Dump_Analysis
decode qcom memory dump

## Environment

window WSL or linux with Python

## Use

- Unzip zip file 
- Put vmlinux and dump file into dir such as Port_COM99

```

 ./ramdump-parser-8909-win-fb.sh Port_COM99
 
 ```
 
 output
 
 ```
 
Start ramdump parser..
cd /mnt/e/qcom-ramdump/tools/linux-ramdump-parser-v2/

python ramparse.py -v /mnt/e/qcom-ramdump/Port_COM99/vmlinux -g /mnt/e/qcom-ramdump/gnu-tools/msm8909/arm-linux-androideabi-gdb  -n /mnt/e/qcom-ramdump/gnu-tools/msm8909/arm-linux-androideabi-gcc-nm  -j /mnt/e/qcom-ramdump/gnu-tools/msm8909/arm-linux-androideabi-objdump -a /mnt/e/qcom-ramdump/Port_COM99 -o /mnt/e/qcom-ramdump/Port_COM99/out -x

/mnt/e/qcom-ramdump/gnu-tools/msm8909/arm-linux-androideabi-gcc-nm: Cannot find plugin 'liblto_plugin.so'

    [1/32] --clock-dump ... 0.647186s
    [2/32] --cpr3-info ... NOTE: 'kryo_regulator_list' list not found to extract kryo_addr information
0.059220s
    [3/32] --cpr-info ... 0.094450s
    [4/32] --cpu-state ... 0.091425s
    [5/32] --ddr-compare ... 2.338783s
    [6/32] --check-for-watchdog ... 0.007905s
    [7/32] --parse-debug-image ... 6.470976s
    [8/32] --dmesg ... 0.251725s
    [9/32] --print-iommu-pg-tables ... 1.641111s
    [10/32] --print-ipc-logging ... FAILED! 0.042723s
    [11/32] --print-irqs ... 1.912554s
    [12/32] --print-kconfig ... 0.008723s
    [13/32] --lpm ... 1.221474s
    [14/32] --print-mdpinfo ... FAILED! 0.022369s
    [15/32] --print-memstat ... 0.057715s
    [16/32] --print-memory-info ... 0.486628s
    [17/32] --dump-page-tables ... 0.049529s
    [18/32] --print-pagealloccorruption ... 0.000516s
    [19/32] --print-pagetracking ... 0.000427s
    [20/32] --print-pagetypeinfo ... 0.765877s
    [21/32] --check-rodata ... 3.671745s
    [22/32] --print-rtb ... 0.010617s
    [23/32] --print-runqueues ... FAILED! 0.574880s
    [24/32] --spm ... 0.290986s
    [25/32] --print-tasks ... FAILED! 0.172338s
    [26/32] --print-tasks-timestamps ... 0.410840s
    [27/32] --check-for-panic ... 0.023886s
    [28/32] --thermal-info ... 0.141615s
    [29/32] --timer-list ... FAILED! 0.307615s
    [30/32] --print-vmalloc ... FAILED! 0.364437s
    [31/32] --print-vmstats ... 0.347852s
    [32/32] --print-workqueues ... 0.375519s

out: /mnt/e/qcom-ramdump/Port_COM99/out
```

you can see the dmesg in dir Out
