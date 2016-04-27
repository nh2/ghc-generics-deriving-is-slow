# ghc-generics-deriving-is-slow

Reproduction for `deriving Generic` being quadratic in the Glorious Haskell Compiler.

## Running

Run `./run.sh`.

Expected output with GHC 7.10.3:

```
➤ ./run.sh 
[1 of 1] Compiling Main             ( Data100.hs, Data100.o )
Linking Data100 ...

real  0m1.089s
user  0m1.012s
sys   0m0.079s
[1 of 1] Compiling Main             ( Data200.hs, Data200.o )
Linking Data200 ...

real  0m2.980s
user  0m2.851s
sys   0m0.150s
[1 of 1] Compiling Main             ( Data400.hs, Data400.o )
Linking Data400 ...

real  0m9.283s
user  0m8.813s
sys   0m0.486s
```

The summary for your convenience:

```
100 alternatives  1 second
200 alternatives  3 seconds
400 alternatives  9 seconds
```
