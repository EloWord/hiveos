<table>
  <tr>
    <td>
      <img width="850" alt="Capture d’écran 2024-01-09 à 14 49 06" src="https://github.com/EloWord/hiveos/assets/155255722/befd116c-1886-488c-90b3-fc9d8e87df8d">
    </td>
    <td>
      <table>
        <tr>
          <td><img height="40" width="150" alt="iconewebsite" src="https://github.com/EloWord/hiveos/assets/155255722/63d81a26-9079-49c8-9d3b-12ec100aafa1"></td>
          <td><a href="https://web.qubic.li/">Qubic Website</a></td>
        </tr>
        <tr>
          <td><img height="40" width="150" alt="iconewallet" src="https://github.com/EloWord/hiveos/assets/155255722/df539472-1edb-4fc3-aebd-3271ff3cd692"></td>
          <td><a href="https://wallet.qubic.li/">Web Wallet</a></td>
        </tr>
        <tr>
          <td><img height="40" width="150" alt="Capture d’écran 2024-01-10 à 01 45 22" src="https://github.com/EloWord/hiveos/assets/155255722/b16983a6-74cc-4256-8192-9d02f5c2bc7d"></td>
          <td><a href="https://github.com/Qubic-Hub/qubic-wallet/releases/">Software Wallet</a></td>
        </tr>
        <tr>
          <td><img height="40" width="150" alt="iconePool" src="https://github.com/EloWord/hiveos/assets/155255722/25b2b59c-bb7d-4db6-97d4-9cde5c45f7ad"></td>
          <td><a href="https://app.qubic.li/public/">Mining Pool</a></td>
        </tr>
      </table>
    </td>
  </tr>
</table>


### Version 1.8.3
- Fixed a bug in calculating local found solutions. (e.g. wrong "SOL: 12/300" display)
- Fixed a reporting bug
- Added experimental display of epoch to console output

Hive OS
- Added new option `"cpuOnly":"yes"` to mine only with your cpu
- Improved it/s reporting in Hive OS Web ui
- Fixed bug on solution reporting in CPU only mining use case
- Improved stability
- Experimental Feature: miner restart and adopt the new Trainer when it receives an update.

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

*Support received since this version: 3,000,000 Qubic - Thank you for your future support!*

[<img src="https://github.com/EloWord/hiveos/assets/155255722/dedb996d-c517-4059-a55a-d9adea9a21f1" alt="discord" width="250">](https://discord.gg/uPP8R6ku)

Thank you for being part of this journey!
<br>

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
<br>

## :wrench: Settings

- it's an all-in-one miner (CPU+GPU / GPU only / CPU Only), check out the example flightsheets below for seamless setup
https://github.com/EloWord/hiveos/releases/download/v-1.8.3/qubic-hivecustom-eloword-v1.8.3.tar.gz

- Recommended GPU overclocks :
**Medium**
3000 series ```nvtool --setcoreoffset 250 --setclocks 1500 --setmem 5001```
4000 series ```nvtool --setcoreoffset 250 --setclocks 2400 --setmem 5001```
**High**
3000 series ```nvtool --setcoreoffset 200 --setclocks 1600 --setmem 7000 --setmemoffset 2000```
4000 series ```nvtool --setcoreoffset 200 --setclocks 2900 --setmem 7000 --setmemoffset 2000```
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
