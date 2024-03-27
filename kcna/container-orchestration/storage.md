# Storage in Containers

Containers revolutionized the way we develop and deploy applications, but they come with a unique challenge: their storage is ephemeral, meaning it doesn't last. Let's break down what this means and how we can work around it.

### What Happens to Storage in a Container?

When you start a container from an image (a kind of blueprint for the container), that image is read-only, containing everything the container needs to run. To allow a container to write files and save changes during its runtime, a temporary, writeable layer is added on top of this read-only image.

![Container Layers](https://d36ai2hkxl16us.cloudfront.net/course-uploads/e0df7fbf-a057-42af-8a1f-590912be5460/mup11dl71nvf-ContainerLayers.png)

However, there's a catch: when the container stops or is deleted, this writeable layer disappears—much like how a computer's memory clears when it's shut down. This setup is great for ensuring consistency and security (since every restart is like starting from scratch), but not so much for saving data.

### Making Data Persist:

To keep data beyond the life of a container, we use something called a **volume**. Volumes are directories on the host system that are mapped into the container, providing a persistent space for data storage. While this does slightly compromise the isolation principle of containers, it's necessary for applications that need to save data.

### Challenges with Data Persistence:

- **Multiple Containers:** What if several containers need access to the same data, or if a container moves to a different server?
- **Consistency and Availability:** Ensuring data is consistently available across containers and hosts.

### Container Orchestration and Storage:

Systems like Kubernetes address these challenges by managing where containers run and how they access persistent storage, ensuring data is available even as containers start and stop.

![Volume Sharing](https://d36ai2hkxl16us.cloudfront.net/course-uploads/e0df7fbf-a057-42af-8a1f-590912be5460/du5zcuxz6i1b-Dataissharedbetweentwocontainersonthesamehost.png)

### Sharing Data Across Containers and Hosts:

Orchestration platforms can set up shared volumes accessible by containers across different hosts, ensuring that necessary data is available regardless of where a container is running.

![Storage is provisioned via a central storage system. Containers on Server A and Server B can share a volume to read and write data](https://d36ai2hkxl16us.cloudfront.net/course-uploads/e0df7fbf-a057-42af-8a1f-590912be5460/0nq859rs7ktv-Storage.png)

### Standardizing Storage Access:

With the rise of various storage solutions (cloud-based, on-premises, etc.), the [Container Storage Interface (CSI)](https://github.com/container-storage-interface/spec) standard was introduced. CSI provides a consistent way to connect containers to storage systems, making it easier to manage and access storage across diverse environments.

In essence, while containers by nature don't hold onto data permanently, solutions like volumes, orchestration systems, and standards like CSI ensure that applications can still save and access the data they need. This setup maintains the agility and efficiency of containers while addressing the need for persistent storage.