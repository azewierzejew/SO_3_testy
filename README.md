użycie:
```bash
#na minixe:
make test-basic
echo <seed> | ./test-basic
```

czekamy aż się skończy i `ps ax | grep test-basic` nic nie wypisze
może zająć z minutę 

ściągamy output.txt

```bash
#na hoście:
./change.py output.txt >myRes<seed>
diff res<seed> myRes<seed>
```
