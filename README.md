# **Shutting Down a Virtual Machine**

Course: DevOps

Mod: Week 1

Topic: Shutting Down a Virtual Machine

Amount of time: 1.5 hours

Author: Thomas Fowler

--------------------------------------------

## **Lesson Objectives**

* Understand the implications when sending an ACPI shutdown
signal to the virtual machine.

* Know the difference between an ACPI shutdown and "powering
off" a virtual machine.

--------------------------------------------

### **Overview**

There are three options to select from when shutting down a
virtual machine: "Saving the State" or suspending a virtual
machine, sending an ACPI (Advanced Configuration and Power
Interface) signal to a virtual machine, and "powering off"
a virtual machine. The two methods discussed in this lesson
are the ACPI shutdown method and the "power off" method.

--------------------------------------------

### **ACPI Shutdown**

When sending an ACPI shutdown signal, the behavior is the
same as if a user depressed the power switch or button on a
desktop PC or laptop computer. This is the preferred way of
shutting down a virtual machine because it allows the
virtual machine to shut down gracefully by properly stopping
virtual hard disks and neatly disposing of other resources
while running.

It should be noted that while the VM shuts down gracefully
via the ACPI shutdown signal, the state of the VM is not
preserved (e.g. open applications, background processes,
etc.). When the VM starts again, all previously open
applications are closed as well as any background services
or daemons not configured to automatically start on boot up.

--------------------------------------------

### **Power Off**

When powering of a virtual machine, the behavior is equivalent
to disconnecting the power source from a physical machine. This
method is the least preferred way of shutting down a virtual
machine and should be used primarily as a last resort if a VM
becomes unstable or unusable for one reason or another. By
abruptly powering off the virtual machine, virtual hard disks
are placed in an inconsistent or volatile state and can
lead to virtual disk corruption and data loss.
