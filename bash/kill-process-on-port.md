# Finding and killing a process running on a port

Find:
```
lsof -i :4200
```

Kill it with:
```
kill -9 <PID>
```
