
<img width="788" alt="Capture d’écran 2024-01-09 à 14 49 06" src="https://github.com/EloWord/hiveos/assets/155255722/befd116c-1886-488c-90b3-fc9d8e87df8d">

### Version 1.8.3
- Fixed a bug in calculating local found solutions. (e.g. wrong "SOL: 12/300" display)
- Fiexd a reporting bug
- Added experimental display of epoch to console output

Hive OS
- Added new option `"cpuOnly":"yes"` to mine only with your cpu
- Improved it/s reporting in Hive OS Web ui
- Fixed bug on solution reporting in CPU only mining
- Improved stability

"Experimental Feature: miner restart and adopt the new Trainer when it receives an update."

****** stay tuned for next release version *******


## :star2: Support My Work and Contribute to its Growth :star2:

If you appreciate my work and want to contribute to its ongoing development, consider leaving a tip. Every contribution, big or small, makes a huge difference and motivates me to continue creating and improving.

- **To support me, use Qubic:** `HJDQLJOMSLGVWAVBWUTRCYPFICUAWTLUBKXLQXOJLBIKTGLRAGQHPDODPQNB`

*Support received since this version: 3,000,000 Qubic - Thank you for your future support!*

[![Join our community on Discord](https://github.com/EloWord/hiveos/assets/155255722/fbc15830-d050-495d-81e7-4947afeebae6?s=200)](https://discord.gg/uPP8R6ku)

Thank you for being part of this journey!


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

*Only NVIDIA GPU compatible*

## Settings:

- it's a all-in-one miner (CPU+GPU / GPU only / CPU Only) use flightsheet exemples down there
https://github.com/EloWord/hiveos/releases/download/v-1.8.3/qubic-hivecustom-eloword-v1.8.3.tar.gz

- Recommended GPU overclocks :
**Medium**
3000 series ```nvtool --setcoreoffset 250 --setclocks 1500 --setmem 5001```
4000 series ```nvtool --setcoreoffset 250 --setclocks 2400 --setmem 5001```
**High**
3000 series ```nvtool --setcoreoffset 200 --setclocks 1600 --setmem 7000 --setmemoffset 2000```
4000 series ```nvtool --setcoreoffset 200 --setclocks 2900 --setmem 7000 --setmemoffset 2000```

## :wrench: Hive OS flightsheet 

Just drop your NVTOOL command in the `Extra config argument` box it's magic

### *** CPU + GPU Dual Flightsheet ***

Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"amountOfThreads":24
"accessToken":"YOUROWNTOKEN"
```
<img width="662" alt="Capture d’écran 2024-01-09 à 14 43 55" src="https://github.com/EloWord/hiveos/assets/155255722/3785f014-affa-4716-aacf-09441b671241">

### *** GPU Only Flightsheet ***

Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"accessToken":"YOUROWNTOKEN"
```
<img width="666" alt="Capture d’écran 2024-01-09 à 14 34 36" src="https://github.com/EloWord/hiveos/assets/155255722/d6473e3b-64be-4251-a5ba-98492e5e7447">

### *** CPU ONLY Flightsheet ***

Extra config arguments exemple:
```
"cpuOnly":"yes"
"amountOfThreads":14
"accessToken":"YOUROWNTOKEN"
```
<img width="664" alt="Capture d’écran 2024-01-09 à 14 42 06" src="https://github.com/EloWord/hiveos/assets/155255722/a755e6e9-677f-48e4-9e3e-1ddf7a2dcc01">
