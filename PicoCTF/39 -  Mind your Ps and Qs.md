# Mind your Ps and Qs

## Descripcion
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
## Pistas
- Bits are expensive, I used only a little bit over 100 to save money
## Solucion
```
python3 RsaCtfTool.py -n 1584586296183412107468474423529992275940096154074798537916936609523894209759157543 -e 65537 --uncipher 964354128913912393938480857590969826308054462950561875638492039363373779803642185
private argument is not set, the private key will not be displayed, even if recovered.                                                  

[*] Testing key /tmp/tmp9j0_xe99.
attack initialized...
attack initialized...
[*] Performing smallq attack on /tmp/tmp9j0_xe99.
[+] Time elapsed: 0.2929 sec.
[*] Performing lucas_gcd attack on /tmp/tmp9j0_xe99.
100%|███████████████████████| 9999/9999 [00:00<00:00, 272670.12it/s]
[+] Time elapsed: 0.0536 sec.
[*] Performing mersenne_primes attack on /tmp/tmp9j0_xe99.
 24%|██████▎                    | 12/51 [00:00<00:00, 364722.09it/s]
[+] Time elapsed: 0.0004 sec.
[*] Performing system_primes_gcd attack on /tmp/tmp9j0_xe99.
100%|██████████████████████| 7007/7007 [00:00<00:00, 1220037.70it/s]
[+] Time elapsed: 0.0297 sec.
[*] Performing pastctfprimes attack on /tmp/tmp9j0_xe99.
100%|████████████████████████| 113/113 [00:00<00:00, 1267262.97it/s]
[+] Time elapsed: 0.0005 sec.
[*] Performing fibonacci_gcd attack on /tmp/tmp9j0_xe99.
100%|███████████████████████| 9999/9999 [00:00<00:00, 259028.87it/s]
[+] Time elapsed: 0.0389 sec.
[*] Performing factordb attack on /tmp/tmp9j0_xe99.
[*] Attack success with factordb method !
[+] Total time elapsed min,max,avg: 0.0004/0.2929/0.0693 sec.

Results for /tmp/tmp9j0_xe99:

Unciphered data :
HEX : 0x007069636f4354467b736d6131315f4e5f6e305f67306f645f37333931383936327d
INT (big endian) : 13016382529449106065927291425342535437996222135352905256639684640304028661985917
INT (little endian) : 3711160986047915108755079562074128500208424285494215969975035182007076726805983232
utf-8 : picoCTF{sma11_N_n0_g0od_73918962}
utf-16 : 瀀捩䍯䙔獻慭ㄱ也湟弰で摯㝟㤳㠱㘹紲
STR : b'\x00picoCTF{sma11_N_n0_g0od_73918962}'

```

## Bandera

picoCTF{sma11_N_n0_g0od_73918962}

## Notas adicionales

## Referencias
