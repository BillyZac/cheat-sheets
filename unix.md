# Unix

## Which process is listening on port 666
Say you install a project, and then run something like `grunt serve` that gives you an error like this:
```
Fatal error: Port 666 is already in use by another process.
```

You can use `lsof`, which shows which process is using that port
```
lsof | grep :666
```

This gives you
```
node      68445 zacharysmith   15u    IPv6 0xf79c11dd4dddafa3        0t0     TCP *:35729 (LISTEN)
```
So we know that `node` is running something, somewhere on this port. But where? 

To answer that, we run the following, `grep`ing for the process ID in the previous result:
```
ps aux | grep 68445
```
Which results in
```
zacharysmith    68445   0.0  0.0  3179560   6008 s000  S+    2:08PM   0:01.77 gulp  
zacharysmith    75488   0.0  0.0  2432772    676 s006  S+   11:40AM   0:00.00 grep 68445
```

The answer is in the first line: `gulp`. (The second line just shows that grep is looking for this number, which we don't really care about.)
