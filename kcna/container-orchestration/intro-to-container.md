# Introduction to Container

## Why Containers?

Application development has always involved finding ways to package and run apps across different platforms and operating systems. Imagine you've created a simple web app using Python. To get this app working, whether on a server or your own computer, there are several steps involved:

1. **Setting Up the Basics:** First, you need to install the operating system and set it up.
2. **Installing Python:** You have to install Python itself, along with any specific extensions your app requires to function.
3. **Networking:** Your system needs to be configured to connect to the internet and other networks.
4. **External Connections:** If your app needs to talk to a database, cache, or storage, you'll have to set up those connections too.

Traditionally, a developer creates the app and knows exactly what it needs to run, but it's often up to a system administrator to actually set up the server, install everything needed, and keep it all running smoothly. This can be tricky and maintenance-heavy, typically resulting in servers being dedicated to just one task (like running a database) and connected through a network.

To make better use of server hardware, **virtual machines (VMs)** came into play. They mimic a full server environment, allowing multiple, isolated servers to run on a single piece of hardware. This was a big step forward, but running many VMs can be inefficient because each one needs its own operating system.

**Enter containers.** Containers offer a neat solution by managing an app's dependencies while being more efficient than using many VMs. Unlike VMs, which emulate entire servers, containers share the host system's operating system but keep the app and its environment isolated. This means you can run many apps in isolation without the overhead of managing multiple operating systems, making everything simpler and more efficient.