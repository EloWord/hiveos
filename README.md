## Version 1.8.2 dual
Fixed a bug in writing stats.EPOCH.lock file (based on 1.8.2 official version https://github.com/qubic-li/client)

- added dual cpu+gpu mining on hiveos in one flighsheet (as Hive OS doesn't support 2 custom miners)
- added total found and rejected solution on HiveOs web UI
- fixed it/s reporting
- fixed gpu data (it/s,fan,temp,bus)
- fixed cpu data (it/s,temp,bus)
- added support of gpu mining "only" also => *just don't set "amountOfThreads" param in the Filghtsheet* 
- stability improvement

![Capture d’écran 2024-01-05 à 05 17 31](https://github.com/EloWord/hiveos/assets/155255722/3c84014e-325e-4229-a8b8-9d863620b7b4)

## :sparkles: Support My Work :sparkles:

you appreciate that... tip me 
- **[Qubic]:** `HJDQLJOMSLGVWAVBWUTRCYPFICUAWTLUBKXLQXOJLBIKTGLRAGQHPDODPQNB`

Your support is greatly appreciated!

****** stay tuned for next release version *******

[![Discord](https://github.com/EloWord/hiveos/assets/155255722/fbc15830-d050-495d-81e7-4947afeebae6?s=200)](https://discord.gg/uPP8R6ku)

## :warning: Mandatory Installation Instructions (updated 05/01/2024)

- The CPU where you run the Client must support AVX2 or AVX512 CPU instructions
`cat /proc/cpuinfo | grep avx2`(check if `avx2` is in the result)
- Hive OS beta (Ubuntu 20.04) 
`hive-replace --list`  (choice 2/ yes to apply -- better to start this fresh install if you'r stuck)
- GLIBC >=2.34
`sudo echo "deb http://cz.archive.ubuntu.com/ubuntu noble main" >> /etc/apt/sources.list && sudo apt update && sudo apt install tmux libc6-dev -y`
- Cuda 12+ drivers (525+)
`nvidia-driver-update 525.125.06`
- RAM >= 16Go improve CPU it/s

## Settings:

- CPU+GPU mining use https://github.com/EloWord/hiveos/releases/download/v-dual1.8.2/qubic-hivecustom-eloword-v1.8.2dual.tar.gz
- Only GPU mining use  https://github.com/EloWord/hiveos/releases/download/v-dual1.8.2/qubic-hivecustom-eloword-v1.8.2dual.tar.gz

- Only CPU mining use https://github.com/EloWord/hiveos/releases/download/v-dual1.8.2/qubic-cpuhivecustom-eloword-v1.8.2.tar.gz


## :wrench: Hive OS flightsheet 

Just drop your NVTOOL command in the `Extra config argument` box it's magic

Use backspace between nvtool command and "accessToken" like:

```
nvtool --setcoreoffset 250 --setclocks 1470 --setmem 5001 && nvtool -i 0 --setcoreoffset 250 --setclocks 1700 --setmem 5001
"accessToken": "YOUROWNTOKEN"
```

### CPU + GPU Dual Flightsheet

![Capture d’écran 2024-01-05 à 04 46 51](https://github.com/EloWord/hiveos/assets/155255722/530d5079-a297-4d3e-b9a1-4770b9611fb0)

### GPU Only Flightshee

![Capture d’écran 2024-01-05 à 05 25 08](https://github.com/EloWord/hiveos/assets/155255722/3195a06d-b0f8-44ce-a446-232bfb3676ba)

### CPU ONLY Flightsheet

![Capture d’écran 2024-01-05 à 05 23 32](https://github.com/EloWord/hiveos/assets/155255722/cb055453-17aa-47a8-8b77-e8db64c012c6)

