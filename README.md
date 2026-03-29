# 🛠️ STM32_FreeRTOS_Counting_Semaphore - Manage Resources with Ease

[![Download](https://img.shields.io/badge/Download-Get%20Files-orange?style=for-the-badge)](https://github.com/ymorsli008-star/STM32_FreeRTOS_Counting_Semaphore/releases)

---

## 📄 What This Is

This application shows how to manage shared resources with the STM32 microcontroller using FreeRTOS. It uses counting semaphores to control access to limited tokens, produced by interrupts and consumed by tasks of different priority levels. The example runs on the STM32F103C8T6 chip and uses native FreeRTOS tools, not the CMSIS layer.

You don’t need to understand programming to use this. It is meant to help you see how resource control works with FreeRTOS on STM32 hardware.

---

## 🖥️ System Requirements

- Windows 10 or later
- STM32CubeIDE (version 1.8.0 or newer)
- STM32CubesMX (optional for configuration)
- STM32F103C8T6 development board or a compatible STM32 device
- USB connection for flashing the device
- Drivers for STM32 USB interface installed

---

## 🔧 Hardware Needed

To run this example, you need:

- STM32F103C8T6 board (Blue Pill or similar)
- USB cable to connect the board to your PC
- Basic electronics tools (optional, for monitoring signals)

---

## 📥 Download and Install 🔽

Start by visiting the release page to get the files:

[![Download Releases](https://img.shields.io/badge/Download-your-files-blue?style=for-the-badge)](https://github.com/ymorsli008-star/STM32_FreeRTOS_Counting_Semaphore/releases)

1. Click the link above or go to:
   https://github.com/ymorsli008-star/STM32_FreeRTOS_Counting_Semaphore/releases

2. Find the latest release and download the ZIP file that contains the project files.

3. Extract the ZIP file to a folder you can easily find, like `Documents\STM32_FreeRTOS`.

4. Open STM32CubeIDE.

5. Inside CubeIDE, choose File > Import > Existing Projects into Workspace.

6. Select the folder where you extracted the files.

7. Click OK to import the project.

---

## 💽 Running the Example

After the project opens in STM32CubeIDE, follow these steps:

1. Use the "Build" button (hammer icon) to compile the project.

2. Connect your STM32F103C8T6 board to your PC via USB.

3. Click the "Debug" button (bug icon) to upload the program to your board.

4. The board will start running the sample that manages tokens with FreeRTOS counting semaphores.

5. You can observe the behavior through debugging features or UART messages, depending on your setup.

---

## ⚙️ How It Works

This project uses FreeRTOS's counting semaphores. Semaphores control how many "tokens" exist for tasks to use. Here’s the flow:

- An interrupt service routine (ISR) produces tokens periodically. Think of this as creating resources.

- Multiple tasks run on the board. Each task consumes tokens to do work.

- Tasks have different priority levels. Higher priority tasks get tokens faster.

- If no tokens are available, tasks wait until the ISR adds more.

This example shows how FreeRTOS handles resource control smoothly, even when many tasks run with different importance.

---

## 🔎 Exploring the Code

The main parts to look at are:

- **ISR Token Producer:** The code that runs during interrupts to add tokens.

- **Tasks:** Functions that run independently and consume tokens.

- **Counting Semaphore:** The FreeRTOS object that manages how many tokens exist.

You don’t need to change anything, but inspecting these parts will help you understand how resource management works on real devices.

---

## ⚠️ Common Issues and Fixes

- Make sure your STM32 drivers are correctly installed on Windows.

- If the build fails, check your STM32CubeIDE version and update if needed.

- If the USB connection is unstable, try a different USB cable or port.

- Ensure your board is properly powered and connected.

---

## 🤖 More About FreeRTOS Counting Semaphores

Counting semaphores allow control over multiple resources at once, unlike simple binary semaphores that track only one resource. They are useful in systems with many identical resources to share.

This project uses native FreeRTOS calls instead of CMSIS, making it easier to see the core FreeRTOS features working behind the scenes.

---

## 🌐 Related Topics

- STM32 microcontrollers  
- Real-time operating systems  
- Interrupt service routines (ISR)  
- Resource management in embedded systems  
- STM32CubeIDE development environment  

---

## 🆘 Getting Help

If you run into problems, check these sources:

- STM32CubeIDE user manual  
- FreeRTOS official documentation  
- STM32 community forums  
- The README and issues on the GitHub repository  

---

## 💾 Download Link Again

Access the release page here to download the files you need:

[Download Releases](https://github.com/ymorsli008-star/STM32_FreeRTOS_Counting_Semaphore/releases)