[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/cakraawijaya/RPI-Basic-Line-Follower-Robot?logo=Codeforces&logoColor=white&color=%23F7DF1E)
![Project](https://img.shields.io/badge/Project-Raspberry-light.svg?style=flat&logo=raspberrypi&logoColor=white&color=%23F7DF1E)
![Type](https://img.shields.io/badge/Type-Personal%20Experiment-light.svg?style=flat&logo=gitbook&logoColor=white&color=%23F7DF1E)

# RPI-Basic-Line-Follower-Robot
Robots are tools that can ease the burden on humans. Robots can be controlled by humans directly, but actually robots can also make their own decisions if given an intelligent algorithm. The type of robot that is often used in school activities is a wheeled robot. A wheeled robot is a robot that moves by using wheels. The purpose of this project is to get a robot that can recognize lines. This project has been implemented and took approximately 3 days. This robot has been equipped with an infrared sensor of the ``` TCRT5000 ``` type. In the process, this sensor works based on the principle of light reflection obtained from the object which is then forwarded to the phototransistor to determine the output value. If the light reflection on a dark or black object is considered inadequate, the sensor module will provide a ``` LOW ``` output, in which case the LED indicator will not light up. If the light reflection on a bright or white surface is considered adequate, the sensor module will provide a ``` HIGH ``` output, in which case the LED indicator will light up. The benefit of making this project is none other than to add insight. The results showed that the system made can function properly.

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | Raspberry Pi Pico |
| Code Editor | Thonny IDE |
| Bootloader | MicroPython UF2 |
| Programming Language | MicroPython |
| Packages | • machine (default)<br>• utime (default) |
| Actuators | Gear Motor / Motor DC (x2) |
| Sensor | KR08200: 3 Way Line Tracking IR Sensor - Brand: Funduino (x1) |
| Other Components | • Micro USB cable - USB type A (x1)<br>• Micro USB cable - 2 pin JST (x1)<br>• Jumper cable (1 set)<br>• KCD11: Rocker Switch SPST (x1)<br>• Li-ion battery 18650 (x2)<br>• 2-Slot series battery holder (x1)<br>• Robot wheels (x2)<br>• Caster wheel (x1)<br>• Motor driver L298N (x1)<br>• Car robot frame (x1)<br>• Spicer bolts (1 set)<br>• Bolts plus (1 set)<br>• Nuts (1 set) |

<br><br>

## Download & Install
1. Thonny IDE

   <table><tr><td width="810">

   ```
   https://bit.ly/ThonnyIDE_Installer
   ```

   </td></tr></table><br>

2. MicroPython UF2

   <table><tr><td width="810">

   ```
   https://bit.ly/UF2_RPIpico_Bootloader
   ```

   </td></tr></table>
   
<br><br>

## Project Designs
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Pictorial Diagram</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Diagram/Block Diagram.jpg" alt="block-diagram"></td>
<td><img src="Assets/Documentation/Diagram/Pictorial Diagram.jpg" alt="pictorial-diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Wiring</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Table/Device Wiring.jpg" alt="wiring"></td>
</tr>
</table>

<br><br>

## MicroPython Bootloader Setup
1. ``` Upload the firmware ``` :

   <table><tr><td width="810">      

      - Press and hold the ``` BOOTSEL ``` button on the ``` Raspberry Pi Pico ``` board while connecting to the computer via a ``` micro USB ``` cable.
   
      - After the ``` Raspberry Pi Pico ``` is recognized by the computer (connected), then immediately release the ``` BOOTSEL ``` button.
      
      - When successfully connected, a new drive called ``` RPI-RP2 ``` will open.
      
      - ``` Drag -> Drop ``` or ``` Copy -> Paste ``` the ``` MicroPython UF2 ``` firmware file into the ``` RPI-RP2 ``` drive.

   </td></tr></table><br>

2. After the process is successful, the ``` RPI-RP2 ``` drive will automatically close.<br><br>

3. In general, the firmware upload only needs to be done once when you first use the ``` Raspberry Pi Pico ``` board.

<br><br>

## Thonny IDE Setup
1. Open ``` Thonny IDE ``` first.<br><br>

2. Click ``` Tools ``` -> then select ``` Options... ``` -> then select :<br><br>
   
   • ``` Interpreter Menu ```, then change the part :

      <table><tr><td width="810">
      
      - ``` Interpreter ``` -> ``` MicroPython (Raspberry Pi Pico) ```
        
      - ``` Port ``` -> ``` Board CDC @ COM... ```
  
      - ``` Restart interpreter before running a script ``` -> ``` uncheck ```

      </td></tr></table>
   
   • ``` Editor Menu ```, then check all the options except: ``` Indent with tab characters ```.<br><br>

3. If the file view does not exist in ``` Thonny IDE ```, then please click the ``` View ``` -> section and select ``` Files ``` to display it.<br><br>

4. Then look for a file called ``` main.py ``` in directory: ``` Raspberry-Pi-Pico-based-Line-Follower-Robot/Src ```.<br><br>
   
5. Right click on the file -> select ``` Upload to / ```.<br><br>

6. Open the file ``` main.py ``` which is in the ``` Raspberry Pi Pico ``` storage -> then click ``` Run current script (F5) ```.<br><br>

7. Program code executed successfully -> sign: ``` %run -c $EDITOR_CONTENT ```.<br><br>

8. If there is still a problem when uploading the program, then try to check the ``` interpreter ``` / ``` port ``` / ``` others ``` section.

<br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>

5. Please enjoy [Done].

<br><br>

## Highlights
<img width="840" src="Assets/Documentation/Experiment/Device.jpg" alt="robot-line-follower">

<br><br>

## Appreciation
If this work is useful to you, then support this work as a form of appreciation to the author by clicking the ``` ⭐Star ``` button at the top of the repository.

<br><br>

## LICENSE
MIT License - Copyright © 2023 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
