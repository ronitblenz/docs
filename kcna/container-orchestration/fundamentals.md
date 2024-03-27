# Fundamentals of Container Technology

## How Containers?

Container technology might seem like a recent innovation, but its roots go way back. In fact, one of the first steps towards modern container technology was the introduction of the `chroot` command with Version 7 Unix in 1979. `Chroot` allows a process to be isolated from the rest of the system's files, effectively creating a "jail" where the process can't access files outside its designated area, even though those files are still on the system.


![Chroot Directory Tree](https://d36ai2hkxl16us.cloudfront.net/course-uploads/e0df7fbf-a057-42af-8a1f-590912be5460/zlgs2h3aa6bl-chrootdirectoriescanbecreatedonvariousplacesinthefilesystem.png)

### Why chroot and containers matter:

- **Chroot:** An early form of process isolation, creating a safe space within the filesystem.
- **Modern Containers:** Today's container technologies build on the `chroot` concept, adding more features for better isolation and efficiency.

### Modern Linux kernels enhance this isolation through ```namespaces``` and ```cgroups``` :

- **Namespaces:** These isolate various system resources (like network interfaces, process IDs, and filesystems) so that processes can operate as if they're running on a separate system.

- **Cgroups:** Stand for control groups, organizing processes hierarchically to manage their system resource allocation (like memory and CPU limits).

**Docker's Role:** Introduced in 2013, Docker didn't invent container technology but made it more accessible and easier to use by integrating existing technologies effectively. Docker is often credited with popularizing containers.

### Containers vs. Virtual Machines (VMs):

- **Virtual Machines:** Emulate entire computers, including hardware and operating systems, which can lead to inefficiencies in resource use and speed.
- **Containers:** More lightweight, sharing the host's kernel and appearing as isolated processes. They start faster and use fewer resources than VMs.

![Traditional Deployment vs Virtualized Deployment vs Container Deployment](https://d36ai2hkxl16us.cloudfront.net/course-uploads/e0df7fbf-a057-42af-8a1f-590912be5460/hzehptn3u06b-TraditionalvsVirtualizedvsContainer.png)

### Deployment Models:

- Traditional deployment had applications running directly on servers, leading to resource conflicts.
- Virtualized deployment uses VMs to isolate applications, improving security and flexibility but with some performance overhead.
- Container deployment allows for efficient, isolated app running environments without the heaviness of full VMs.

In practice, containers and VMs often work together, combining the efficiency and speed of containers with the secure isolation of VMs. This hybrid approach leverages the best of both worlds for modern application deployment.