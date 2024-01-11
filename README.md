<table>
  <tr>
    <td>
      <img width="850" alt="Capture d’écran 2024-01-09 à 14 49 06" src="https://github.com/EloWord/hiveos/assets/155255722/b88dd2ed-77f6-45a2-86e9-9531f9628b03">
    </td>
    <td>
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
    </td>
  </tr>
</table>

### Version 1.8.4: 
- Enhanced Logging for GPU it/s

Hive OS:
- Resolved issues with GPU hashrate reporting in the HiveOS Web UI.
- Introduced a new feature: In cases where individual GPU it/s are not reported, HiveOS will now display an average of the total GPU it/s.

*Known Bug Alert: GPU#0 its display may show a decrease, but rest assured, the actual hashrate remains stable. This is strictly a display issue and will be resolved in the upcoming release*


****** Get ready for the next exciting update - coming soon! *******

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

- **To support me, use Qubic:** `HJDQLJOMSLGVWAVBWUTRCYPFICUAWTLUBKXLQXOJLBIKTGLRAGQHPDODPQNB`

*Support received since this version: 6,000,000 Qubic - Thank you for your future support!*

[<img src="https://github.com/EloWord/hiveos/assets/155255722/dedb996d-c517-4059-a55a-d9adea9a21f1" alt="discord" width="200">](https://discord.gg/uPP8R6ku)

Thank you for being part of this journey!
<br>

## :warning: Mandatory Installation Instructions (updated 11/01/2024)

- The CPU where you run the Client must support AVX2 or AVX512 CPU instructions
`cat /proc/cpuinfo | grep avx2`(check if `avx2` is in the result)
- Hive OS beta (Ubuntu 20.04) 
`hive-replace --list`  (choice 2/ yes to apply -- better to start this fresh install if you'r stuck)
- GLIBC >=2.34 (updated 11/01/2024)
`apt update && apt upgrade && echo "deb http://cz.archive.ubuntu.com/ubuntu jammy main" >> /etc/apt/sources.list && apt update && apt install tmux -y && sudo apt install libc6 -y `
- Cuda 12+ drivers (525+)
`nvidia-driver-update 525.125.06`
- RAM >= 16Go improves CPU it/s

*Only NVIDIA GPU compatible*
<br>

## :wrench: Settings

- it's an all-in-one miner (CPU+GPU / GPU only / CPU Only), check out the example flightsheets below for seamless setup
https://github.com/EloWord/hiveos/releases/download/v1.8.4/eloword-v1.8.4.tar.gz

- Recommended GPU overclocks :
**Medium**
3000 series `nvtool --setcoreoffset 250 --setclocks 1500 --setmem 5001`
4000 series `nvtool --setcoreoffset 250 --setclocks 2400 --setmem 5001`
**High**
3000 series `nvtool --setcoreoffset 200 --setclocks 1600 --setmem 7000 --setmemoffset 2000`
4000 series `nvtool --setcoreoffset 200 --setclocks 2900 --setmem 7000 --setmemoffset 2000`
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

![1](https://github.com/EloWord/hiveos/assets/155255722/507ea22b-bd09-4cf1-a11c-44962b071318)

### *** GPU Only Flightsheet ***

Extra config arguments exemple:
```
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 7000 --setmemoffset 2000
"accessToken":"YOUROWNTOKEN"
```
![2](https://github.com/EloWord/hiveos/assets/155255722/0093841c-fc14-446e-9e94-4ce737842040)


### *** CPU ONLY Flightsheet ***

Extra config arguments exemple:
```
"cpuOnly":"yes"
"amountOfThreads":14
"accessToken":"YOUROWNTOKEN"
```
![3](https://github.com/EloWord/hiveos/assets/155255722/494cc63e-2bf6-4596-9983-6eec40b1cbf8)

