# NachOS Tasks — How to Run

## Task 1: Abs System Call
```bash
# Build test program
cd nachos-project-master/code/test
make abs

# Build NachOS kernel
cd ../build.linux
make

# Run
./nachos -x ../test/abs
```

**Expected output:** `42`

---

## Task 2: Priority Scheduler
```bash
# Build NachOS kernel
cd nachos-project-master/code/build.linux
make

# Run thread self-test
./nachos -K
```

**Expected output:**
```
--- Priority Scheduler Test ---
*** thread priority 10 running
*** thread priority 5 running
*** thread priority 1 running
--- Priority Scheduler Test Done ---
```

---

## Task 3: Sleep System Call
```bash
# Build NachOS kernel
cd nachos-project-master/code/build.linux
make

# Build test program
cd ../test
make sleep_test

# Run
cd ../build.linux
./nachos -x ../test/sleep_test
```

**Expected output:** Slept ticks close to 1000 (within 100 ticks due to timer granularity)
