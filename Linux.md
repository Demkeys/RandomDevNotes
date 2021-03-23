----
### Linux program execution process | What does a C program main function returns to

* What happens when you run a program? https://stackoverflow.com/questions/1204078/what-happens-when-you-run-a-program
* What happens when a computer program runs? https://stackoverflow.com/questions/5162580/what-happens-when-a-computer-program-runs
* Difference between exit() and return in main() function in C https://stackoverflow.com/questions/35471878/difference-between-exit-and-return-in-main-function-in-c
* Exit program x86 https://stackoverflow.com/questions/32415331/exit-program-x86
----
### How an OS loads and executes a program? (Applies to Windows & Linux)
* https://medium.com/cracking-the-data-science-interview/how-operating-systems-work-10-concepts-you-should-know-as-a-developer-8d63bb38331f
* https://en.wikipedia.org/wiki/Loader_(computing)
* https://stackoverflow.com/questions/32688459/how-does-a-loader-in-operating-system-work
* https://stackoverflow.com/questions/55786222/how-is-a-program-loaded-in-os
* https://stackoverflow.com/questions/5570893/how-does-a-system-call-translate-to-cpu-instructions
* https://stackoverflow.com/questions/31722881/is-an-entire-static-program-loaded-into-memory-when-launched
* https://stackoverflow.com/questions/1599434/how-does-program-execute-where-does-the-operating-systems-come-into-play
* https://stackoverflow.com/questions/12931632/how-does-os-execute-compiled-binary-files
* https://stackoverflow.com/questions/1599434/how-does-program-execute-where-does-the-operating-systems-come-into-play
----
### ANSI, C and Escape Sequences

* https://stackoverflow.com/questions/45612822/how-to-properly-add-hex-escapes-into-a-string-literal
* https://stackoverflow.com/questions/38482586/unknown-escape-sequence
* https://stackoverflow.com/questions/56284599/why-must-i-use-x1b-not-to-represent-an-escape-character
* https://stackoverflow.com/questions/3219393/stdlib-and-colored-output-in-c
* https://en.wikipedia.org/wiki/Escape_sequence
* https://en.wikipedia.org/wiki/Escape_sequences_in_C#Table_of_escape_sequences
* https://en.wikipedia.org/wiki/ANSI_C
* https://en.wikipedia.org/wiki/ANSI_escape_code
* https://en.wikipedia.org/wiki/Geometric_Shapes


Notes about escape sequences in C:
* \x is an escape sequence whereas 0x would be a hex literal.
* And escape sequence string can consist of chars or hex values. "\x1b[31m" can be written as "\x1b\x5b\x33\x32\x6d". In "\x1b[31m" 1b is hex for the ESC control code (since there is no way to enter ESC control code through the keyboard), whereas [31m are individual chars.
----
### What are .cfi directives in GCC Assembly output and how to strip them from output?
* https://stackoverflow.com/questions/2529185/what-are-cfi-directives-in-gnu-assembler-gas-used-for
* https://stackoverflow.com/questions/38552116/how-to-remove-noise-from-gcc-clang-assembly-output/38552509
----
### C Anonymous Enums
* https://stackoverflow.com/questions/1821341/unnamed-enum-typedef
* https://stackoverflow.com/questions/7147008/the-usage-of-anonymous-enums
* https://stackoverflow.com/questions/10157181/in-which-situations-anonymous-enum-should-be-used
* https://docs.microsoft.com/en-us/cpp/c-language/c-enumeration-declarations?view=vs-2019
---
### BIOS, UEFI, How BIOS boot works, How UEFI boot works
* https://stackoverflow.com/questions/58002542/how-does-uefi-boot-mode-boot-flows
* https://stackoverflow.com/questions/32223339/how-does-uefi-work
* https://superuser.com/questions/344954/what-mode-do-modern-64-bit-intel-chip-pcs-run-the-boot-sector-in/345333#345333
* https://superuser.com/questions/731362/how-does-efi-find-bootloaders
* https://superuser.com/questions/496026/what-is-the-difference-in-boot-with-bios-and-boot-with-uefi
* https://en.wikipedia.org/wiki/Real_mode
* https://stackoverflow.com/questions/58651734/do-modern-computers-boot-in-real-mode-or-virtual-real-mode
* https://askubuntu.com/questions/993269/difference-between-legacy-bios-and-uefi
* https://en.wikipedia.org/wiki/Booting#Modern_boot_loaders
* https://en.wikipedia.org/wiki/Booting#Boot_sequence
* https://en.wikipedia.org/wiki/Comparison_of_boot_loaders
* https://en.wikipedia.org/wiki/BIOS
* https://en.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface#Disk_device_compatibility
* https://en.wikipedia.org/wiki/EFI_system_partition#Linux
----
### X11 Server, Xlib, and using X to show a window and draw shapes in the window
* https://github.com/QMonkey/Xlib-demo (NOTE: For some reason the code provided here doesn't work as it is. The next link gives a solution to this problem.)
* https://stackoverflow.com/questions/18098678/weird-ass-xlib-bug-xdrawstring-only-works-after-a-sleep
* https://stackoverflow.com/questions/16835128/x-window-always-blank
* https://stackoverflow.com/questions/16688368/how-a-draw-a-string-in-a-splash-screen-by-xlib
* https://stackoverflow.com/questions/31286404/execution-of-sleep-in-xlib-programming
* https://stackoverflow.com/questions/31088029/flushing-events-to-x11
* https://stackoverflow.com/questions/45315318/xlib-wont-draw-anything
* https://www.x.org/releases/X11R7.7/doc/libX11/libX11/libX11.html
* https://stackoverflow.com/questions/29316148/c-x11-api-graphics-not-working-in-a-while-loop
* https://en.wikibooks.org/wiki/X_Window_Programming/Xlib
----
### Using DirectX libraries with C
* https://gamedev.stackexchange.com/questions/62690/is-it-possible-to-use-directx-in-pure-c-program
* Quake, example of a game written in C that uses DirectX: https://github.com/id-Software/Quake
* https://stackoverflow.com/questions/4696079/directx-programming-in-c
----
### Writing an x86 bootloader (GAS syntax, run in QEMU)
* https://medium.com/@g33konaut/writing-an-x86-hello-world-boot-loader-with-assembly-3e4c5bdd96cf
* This is my repo with some basic bootloader examples: https://github.com/Demkeys/x86-Assembly-ATT-Bootloaders
