# F4BPP Icom IC-PCR100 Remote Software

## 1. Presentation of the software.

![F4BPP Icom IC-PCR100 Preview](https://github.com/f4bpp/Icom_IC-PCR100_Remote_Software/blob/main/Images/F4BPP_Icom_IC-PCR100_Remote_Software_Preview.png)

Icom IC-PCR100 Remote is a program designed for the Linux environment.

It has been developed to optimise the reception of SSTV images sent from the ISS by astronauts. It therefore has two buttons to launch Gpredict and QSSTV respectively from the program.

 - Gpredict is a software package for tracking and predicting satellite orbits in real time. 
   
 - QSSTV is software for decoding SSTV (Slow Scan Television) images.

Thanks to the interconnection between the Icom IC-PCR100 and Gpredict, the receiver's reception frequency is adjusted in real time to correct the Doppler effect inherent in satellite communications: higher frequency when the satellite is approaching and lower frequency when it is moving away

## 2. Prerequisites for running the software.

To run, this programme requires the following packages to be installed: **libhamlib-utils**.

With the **libhamlib-utils** package, which includes the **rigctld** software, Gpredict can take control of the Icom IC-PCR100 using the terminal and a simple command line. However, the user has no control over settings such as volume, squelch and reception mode (FM, WFM and AM). Moreover, there is no indication to the user that the receiver frequency is correctly adjusted by Gpredict.

The Icom IC-PCR100 remote software allows the user to take control of the receiver via a graphical interface without using the terminal. It also allows the user to control the volume, squelch and receive mode while Gpredict takes control of the VFO to adjust the frequency.

The **Gpredict** software is therefore also necessary if you want to use the receiver to receive satellites or the International Space Station.

If you wish to receive SSTV images sent from space via the ISS, you will also need to install the **QSSTV** software.

## 3. Software installation.

To install the Icom IC-PCR100 remote software, simply double-click on the package and let the package installer of your Linux distribution guide you.

You can also open a terminal at the location where you downloaded the software and enter the following command for the desktop version:

    sudo dpkg -i PCR100_Remote_amd64.deb

For the Raspberry PI version, enter the following command:

    sudo dpkg -i PCR100_Remote_arm64.deb

## 4. Connecting the receiver to the computer.

The icom IC-PCR100 is a receiver that was launched in 1998. At the time, it was supplied with a DB9 connection cable, also known as an RS-232 COM port. This type of port is no longer found on computers.

Instead, you need a USB/RS232 converter cable, which is often fitted with an FTDI-232RL chip. This adapter enables the computer to communicate with the receiver via a USB port.

The ICOM IC-PCR100 Remote software can control the receiver via your computer's USB ports, but will be unable to detect it if you are using an RS-232 port.
