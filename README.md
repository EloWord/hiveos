Latest Release : [https://github.com/EloWord/hiveos/releases/tag/1.8.2dualfix1](https://github.com/EloWord/hiveos/releases/tag/1.8.2dualfix1)

- Improved HiveOs version compatibility
- Improved it/s reporting
- Fixed bug on solution reporting when GPU only mining
- Fixed bug on uptime reporting

****** stay tuned for next release version *******

![Capture d’écran 2024-01-05 à 05 17 31](https://github.com/EloWord/hiveos/assets/155255722/3c84014e-325e-4229-a8b8-9d863620b7b4)

## :star2: Support My Work and Contribute to its Growth :star2:

If you appreciate my work and want to contribute to its ongoing development, consider leaving a tip. Every contribution, big or small, makes a huge difference and motivates me to continue creating and improving.

- **To support me, use Qubic:** `HJDQLJOMSLGVWAVBWUTRCYPFICUAWTLUBKXLQXOJLBIKTGLRAGQHPDODPQNB`

*Support received since this version: 0 Qubic - Thank you for your future support!*

[![Join our community on Discord](https://github.com/EloWord/hiveos/assets/155255722/fbc15830-d050-495d-81e7-4947afeebae6?s=200)](https://discord.gg/uPP8R6ku)

Your support is greatly appreciated. Thank you for being part of this journey!


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

- CPU+GPU mining use https://github.com/EloWord/hiveos/releases/download/1.8.2dualfix1/qubic-hivecustom-eloword-v1.8.2dualfix1.tar.gz
- Only GPU mining use https://github.com/EloWord/hiveos/releases/download/1.8.2dualfix1/qubic-hivecustom-eloword-v1.8.2dualfix1.tar.gz

- Only CPU mining use https://github.com/EloWord/hiveos/releases/download/v-dual1.8.2/qubic-cpuhivecustom-eloword-v1.8.2.tar.gz


## :wrench: Hive OS flightsheet 

Just drop your NVTOOL command in the `Extra config argument` box it's magic

*Use backspace between nvtool command and "accessToken"*


### CPU + GPU Dual Flightsheet

Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"amountOfThreads":14
"accessToken": "YOUROWNTOKEN"
```

![Capture d’écran 2024-01-05 à 04 46 51](https://github.com/EloWord/hiveos/assets/155255722/530d5079-a297-4d3e-b9a1-4770b9611fb0)

### GPU Only Flightsheet


Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"accessToken": "YOUROWNTOKEN"
```

![Capture d’écran 2024-01-05 à 05 25 08](https://github.com/EloWord/hiveos/assets/155255722/3195a06d-b0f8-44ce-a446-232bfb3676ba)

### CPU ONLY Flightsheet

Extra config arguments exemple:
```
"amountOfThreads":14
"accessToken": "YOUROWNTOKEN"
```

![Capture d’écran 2024-01-05 à 05 23 32](https://github.com/EloWord/hiveos/assets/155255722/cb055453-17aa-47a8-8b77-e8db64c012c6)

