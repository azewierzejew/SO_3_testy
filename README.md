użycie: (seedy na razie to 1, 2, 3, 4)
```bash
#na minixe:
make test-basic
rm part_output*.txt
echo <seed> | ./test-basic
```

Czekamy aż się skończy i `ps ax | grep test-basic` nic nie wypisze poza samym sobą (czyli tam coś `..... grep test-basic`.
Bo mogłoby jeszcze wypisywać jakieś `./test-basic` gdyby nie wszystkie potomki skończyły.
Może zająć z minutę.

```bash
#na minixie:
cat part_output*.txt >output.txt
```

ściągamy output.txt

```bash
#na hoście:
./change.py output.txt >myRes<seed>

# dla zwykłej wersji
diff res<seed> myRes<seed>
# albo dla uproszczonej
diff res<seed>_alt myRes<seed>
```
