<img width="988" alt="Capture d’écran 2024-01-19 à 13 08 26" src="https://user-images.githubusercontent.com/155255722/298063346-3a030ae9-fdf2-418b-b857-ca570d72ddf5.png">

### Hiveos
- Optimized the number of hugepages in HiveOS system environment for the new AI training algorithm.
- Enhanced overall stability and security.
- Resolution of an issue encountered when operating another HiveOS miner within the same flight sheet
- Correction of a bug associated with altering the CPU's thread count, specifically "amountOfThreads" option
- Optimized binaries and librairies requirments for upcoming HiveOS integration

Use now in Flightsheet: https://github.com/EloWord/hiveos/releases/download/v1.8.6rev1/eloword-v1.8.6rev1.tar.gz

****** Get ready for the next exciting update - coming soon! *******

<table>
        <tr>
          <td><img height="30" width="120" alt="iconewebsite" src="https://github.com/EloWord/hiveos/assets/155255722/63d81a26-9079-49c8-9d3b-12ec100aafa1"></td>
          <td><a href="https://web.qubic.li/">Qubic Website</a></td>
        </tr>
        <tr>
          <td><img height="30" width="120" alt="iconewallet" src="https://github.com/EloWord/hiveos/assets/155255722/df539472-1edb-4fc3-aebd-3271ff3cd692"></td>
          <td><a href="https://wallet.qubic.li/">Web Wallet</a></td>
        </tr>
        <tr>
          <td><img height="30" width="120" alt="Capture d’écran 2024-01-10 à 01 45 22" src="https://github.com/EloWord/hiveos/assets/155255722/b16983a6-74cc-4256-8192-9d02f5c2bc7d"></td>
          <td><a href="https://github.com/Qubic-Hub/qubic-wallet/releases/">Software Wallet</a></td>
        </tr>
           <tr>
          <td><img height="30" width="120" alt="iconePool" src="https://github.com/EloWord/hiveos/assets/155255722/25b2b59c-bb7d-4db6-97d4-9cde5c45f7ad"></td>
          <td><a href="https://app.qubic.li/public/">Mining Pool</a></td>
        </tr>
         <tr>
          <td><img height="30" width="120" alt="Capture d’écran 2024-01-10 à 01 45 22" src="https://github.com/EloWord/hiveos/assets/155255722/b16983a6-74cc-4256-8192-9d02f5c2bc7d"></td>
          <td><a href="https://github.com/qubic-li/client?tab=readme-ov-file#download">Official Cient</a></td>
        </tr>
</table>


<!--
|  | Usefull Links |
| ---- | --------- |
| <img height="40" width="160" alt="iconewebsite" src="https://github.com/EloWord/hiveos/assets/155255722/63d81a26-9079-49c8-9d3b-12ec100aafa1"> | [Qubic Website](https://web.qubic.li/) | 
| <img height="40" width="160" alt="iconewallet" src="https://github.com/EloWord/hiveos/assets/155255722/df539472-1edb-4fc3-aebd-3271ff3cd692"> | [Web Wallet](https://wallet.qubic.li/) | 
| <img height="40" width="160" alt="Capture d’écran 2024-01-10 à 01 45 22" src="https://github.com/EloWord/hiveos/assets/155255722/b16983a6-74cc-4256-8192-9d02f5c2bc7d"> | [Software Wallet](https://github.com/Qubic-Hub/qubic-wallet/releases/) | 
|<img height="40" width="160" alt="iconePool" src="https://github.com/EloWord/hiveos/assets/155255722/25b2b59c-bb7d-4db6-97d4-9cde5c45f7ad"> | [Mining Pool](https://app.qubic.li/public/) |
-->
<br>

## :star2: Support My Work and Contribute to its Growth :star2:

If you appreciate my work and want to contribute to its ongoing development, consider leaving a tip. Every contribution, big or small, makes a huge difference and motivates me to continue creating and improving.

- **To support me, use Qubic:** `QYGPXYBKNIDKVFFUWMMJFPWNMPXAPAVFEFEJOTUEIALMQZEFNKXOUUQEWBOM`

*Support received since this version: 620,240,488 Qubic - Thank you for your future support!*

[<img src="https://github.com/EloWord/hiveos/assets/155255722/dedb996d-c517-4059-a55a-d9adea9a21f1" alt="discord" width="200">](https://discord.gg/bWHcuuyQBf)

Thank you for being part of this journey!
<br>

## :warning: Mandatory Installation Instructions
- The CPU where you run the Client must support AVX2 or AVX512 CPU instructions
`cat /proc/cpuinfo | grep avx2`(check if `avx2` is in the result)
- Hive OS beta (Ubuntu 20.04) 
`/hive/sbin/hive-replace --list`  (choice 2/ yes to apply -- better to start this fresh install if you'r stuck)
- GLIBC >=2.34
```apt update && apt upgrade -y && echo "deb http://archive.ubuntu.com/ubuntu jammy main" >> /etc/apt/sources.list && apt update && apt install tmux -y && apt install libc6 -y``` (answer yes to any question)
- Cuda 12+ drivers (525+) 
- Cuda 12 for 1000 series must be 535+
`nvidia-driver-update 535.146.02` (or newer)
- RAM >= 16Go improves CPU it/s
- Higher RAM frequencies improves CPU it/s
- Do not overload your CPUs with threads, instead, aim to find the sweetpoint

*Only NVIDIA GPU compatible*
<br>

## :wrench: Settings

- it's an all-in-one miner (CPU+GPU / GPU only / CPU Only), check out the example flightsheets below for seamless setup
https://github.com/EloWord/hiveos/releases/download/v1.8.6rev1/eloword-v1.8.6rev1.tar.gz

- Recommended GPU overclocks :
**Medium**
3000 series ```nvtool --setcoreoffset 250 --setclocks 1500 --setmem 5001```
4000 series ```nvtool --setcoreoffset 250 --setclocks 2400 --setmem 5001```
**High**
3000 series ```nvtool --setcoreoffset 200 --setclocks 1600 --setmem 7000 --setmemoffset 2000```
4000 series ```nvtool --setcoreoffset 200 --setclocks 2900 --setmem 7000 --setmemoffset 2000```
<br>

- Extra config arguments Box (options):

| Setting | Description |
| ---- | --------- |
| ```"accessToken":``` | This is you personal JWT Token which you can obtain from the Control Panel at qubic.li |
| ```"payoutId":``` |  This is the ID you want to get token payout for your found solutions. |
|  ```"overwrites": {"AVX512": false}``` |  Disable AVX512 and enforce AVX2 (AVX Intel CPU not working) |
| ```"overwrites": {"SKYLAKE": true}```  |  Enforce SKYLAKE (AVX Intel CPU not working)  |
<br>

## ✈️ Hive OS flightsheet 

Just drop your NVTOOL command in the `Extra config argument` box it's magic

### *** CPU + GPU Dual Flightsheet ***

Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"amountOfThreads":24
"accessToken":"YOUROWNTOKEN"
```
![1](https://github.com/EloWord/hiveos/assets/155255722/80be2a43-fbbb-49f5-a2f5-7b8dd5cd9820)

### *** GPU Only Flightsheet ***

Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"accessToken":"YOUROWNTOKEN"
```
![2](https://github.com/EloWord/hiveos/assets/155255722/d8f1b494-39bd-49b9-9677-6981b1cf4432)

### *** CPU ONLY Flightsheet ***

Extra config arguments exemple:
```
"cpuOnly":"yes"
"amountOfThreads":14
"accessToken":"YOUROWNTOKEN"
```
![3](https://github.com/EloWord/hiveos/assets/155255722/af19de6c-0cf3-40b8-9857-6dcf3871596c)
