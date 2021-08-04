# eBPF
Program kernel to enable eBPF
To Compile
clang $(CFLAGS) -o $(EXECABLE) -lelf $(LOADINCLUDE) $(LIBRARY_PATH) $(BPFSO) \
        $(BPFLOADER) loader.c

clang -O2 -target load -lelf -c loader.c -o loader1

clang -O2 -target bpf -c bpf_load.c -o loader12

clang -O2 -o loader16 -l elf -I/usr/include -I/usr/include/bpf bpf_load.c loader.c
