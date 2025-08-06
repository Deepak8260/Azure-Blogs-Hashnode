---
title: "Day2 - What Is Cloud Computing and Intro To IP Address"
seoTitle: "Cloud Computing Basics and IP Addresses"
datePublished: Wed Aug 06 2025 18:42:11 GMT+0000 (Coordinated Universal Time)
cuid: cme0beuma000t02jvbmtdhm38
slug: day2-what-is-cloud-computing-and-intro-to-ip-address
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1754505704094/d30d6042-3091-4ecc-8130-f71df3545f50.png
tags: azure, cloud-computing, hyper-v, mac-address, ip-address, ipaddress, arpanet

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754505583924/a2f47a46-b0f7-4705-855c-67c9ba31bde0.png align="center")

### **Let’s Begin With a Simple Thought – Why Virtualization**

A physical server or even a standard laptop is typically limited to running a single operating system at a time. For instance, by default, it's not possible to run Windows and Linux simultaneously on the same physical machine.

However, this limitation can be overcome through virtualization technologies such as VMware or similar platforms. These tools enable the simultaneous operation of multiple operating systems on a single physical device, making use of virtualization techniques behind the scenes.

This marks the essence of virtualization — a method that expands the capabilities of physical systems by allowing them to perform tasks that were previously restricted or impossible.

### **What Exactly Is Virtualization?**

So let’s define it :

**“It is the technique of splitting physical resources into logical resources.”**

That’s it. Simple line.

When you apply virtualization on a **physical server**, you get multiple **logical environments** on the same hardware. And each of these environments behaves like a complete standalone machine.

### **Let's Take a Practical Example:**

Take your **laptop**. Normally, you install one OS – Windows.

But what if you also want to run **Linux** alongside it?

* You can’t do it natively.
    
* You can dual boot, but only one OS runs at a time.
    

But with virtualization, using tools like VMware or VirtualBox, you can **run Linux inside Windows**. That Linux OS believes it’s on its own computer. But no! It’s inside your laptop. That’s virtualization.

So, this process where:

* You create **multiple environments** (Linux, RedHat, Ubuntu)
    
* On a **single piece of hardware** (your laptop)
    
* And all run **simultaneously**, independently
    

This is **virtualization in real life**.

### **Let’s Translate That to Real Servers:**

What we just discussed applies in a data center too.

In an enterprise, you can take a physical server and apply virtualization. This way, one physical server can host:

* 10 virtual servers
    
* Each with their own OS and applications
    

And it saves money. Instead of buying 10 physical servers, you **run 10 virtual ones** on a single machine.

Now comes the main player here – the **hypervisor**.

### **What Is a Hypervisor?**

When you want to virtualize your physical machine, you need a piece of software. This is called a **hypervisor**.

What does it do?

* It **sits on top of your physical server**
    
* It lets you create, run, and manage virtual machines
    
* It **allocates resources** to VMs (like RAM, CPU, storage)
    

There are two types of hypervisors:

#### **Type 1 Hypervisor (Bare Metal):**

* Installed directly on the physical machine
    
* Doesn’t need an underlying OS
    
* Much more powerful and secure
    
* Used in real-world production environments
    

| Cloud Platform | Hypervisor Type |
| --- | --- |
| Azure | Hyper-V |
| AWS | Xen, Nitro |
| VMware | ESXi |

#### **Type 2 Hypervisor (Hosted):**

* Installed on top of an existing operating system
    
* Suitable for training or learning
    
* Used on laptops for testing
    

Examples:

* VMware Workstation
    
* Oracle VirtualBox
    

But let me be very clear: **In real cloud computing**, **we use Type 1 only**.

For more, refere to this blog [https://kdazureblogs.hashnode.dev/day1-introduction-to-cloud-computing](https://kdazureblogs.hashnode.dev/day1-introduction-to-cloud-computing)

## **Scaling Virtualization to a Data Center – The Cloud Backbone**

So far, we have understood what virtualization is.

We’ve seen how, using a hypervisor on our personal laptop or system, we can create multiple virtual machines (VMs). Each of these virtual machines can run its own operating system, its own applications, and work independently — all inside a single physical device like a laptop.

This means, instead of needing three different laptops to run Windows, Ubuntu, and RedHat Linux separately, you can just have one good laptop, and run all three **together** using virtualization.

This is great for learning and development — but now comes the real question:

What happens when we apply this idea at a **much larger scale**?

Let’s now take this concept — the idea of virtualization — and **move it from your laptop to a real-world cloud data center**, like the ones used by **Microsoft Azure**, **Amazon AWS**, or **Google Cloud**.

### **What Is a Data Center?**

A **data center** is a huge physical building — sometimes as large as a football stadium — built specifically to host thousands and thousands of powerful computers. These computers are not ordinary ones like our laptops; they are **special enterprise-grade physical servers**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754501675686/006ac17b-0406-4da6-8959-ee9c2e220335.png align="center")

If you could walk into such a data center, here’s what you’d see:

* The entire space is filled with **metal racks**.
    
* Each rack holds **multiple physical servers**, stacked one over another.
    
* There are **rows and rows of these racks**, running all the time.
    
* There are blinking lights, cooling fans, and a deep humming sound in the background — the sound of the cloud working silently behind the scenes.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754501692997/d4ad0523-1868-4d65-a19d-f2adbbcb5530.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754501796819/8f3798ae-4e37-448a-bedb-336583721858.png align="center")

This building is kept cool with air conditioning, protected by security, monitored 24x7, and connected to the fastest internet lines available.

### **Now Imagine This…**

Let’s say Microsoft has one such data center, and it has **10,000 physical servers** inside.

Each server:

* Has massive RAM — maybe 1 TB (terabyte)
    
* Dozens of CPUs — even 128 cores
    
* High-speed SSD storage — several terabytes
    

Now, by default, each of these servers can run **only one operating system** at a time — just like your laptop.

But that would be a complete waste of resources, right? Why run only one program or one OS on such a powerful machine?

So here’s what Microsoft does…

### **Applying Virtualization in the Data Center**

Microsoft installs a **hypervisor** on each of those physical servers.

Yes — the same hypervisor concept you learned earlier. But this time, it's not the Type 2 version (used for learning). It’s the real one — **Type 1 hypervisor**, like **Hyper-V** in Microsoft’s case.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754501814198/9047e7c6-b877-45fe-a94a-01d2074380cf.jpeg align="center")

Once the hypervisor is installed, each of these physical servers becomes a **Virtualization Host**.

Now what happens?

This one single physical server can now run **multiple virtual machines** — just like your laptop did, but now at an enterprise level.

Here’s an example:

Suppose one of these servers has:

* 1 TB (1024 GB) RAM
    
* 128 CPU cores
    
* 10 TB SSD storage
    

Using the hypervisor, Microsoft can create:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754501824278/7edbe775-d386-4e11-af84-a77a3a2e7b00.png align="center")

* 100 virtual machines on this one server
    
* Each VM can be assigned:
    
    * 8 GB or 16 GB RAM
        
    * 2 or 4 virtual CPUs
        
    * 100 GB of storage
        
* Each VM runs its own operating system — Linux, Windows, Ubuntu, RedHat, etc.
    

So what’s the result?

A single physical machine becomes **home to 100+ virtual machines**, and all of them are running **simultaneously**, completely isolated from one another.

### **Who Uses These Virtual Machines?**

Now you may wonder — who is using these virtual machines?

Here comes the most important part.

Each of these virtual machines is being **rented by a customer**.

Let’s say:

* One VM is being used by a software company to host their website.
    
* Another VM is used by a startup to run a backend application.
    
* Another one is used by a bank for storing customer transactions.
    
* One might be a Linux server for a data science student.
    
* Another might be a Windows server for hosting an ERP system.
    

And all these VMs are running **on the same physical server** in the data center — yet they never interfere with each other.

They’re completely isolated, secure, and feel like **individual computers** to their respective users.

That’s the magic of virtualization at scale.

### **What Happens When You Click “Create Virtual Machine” on Azure?**

Now let’s come to you.

You are sitting at your home or office.

You open your laptop, go to a browser, and open this website:  
👉 [`https://portal.azure.com`](https://portal.azure.com)

You log in to your Azure account.

From there, you click on “Create a Virtual Machine.”

Azure now shows you options to select:

* Operating System (e.g., Ubuntu, Windows Server)
    
* Size of the machine (e.g., DS1 v2, 2 vCPUs, 8 GB RAM)
    
* Region (e.g., Southeast Asia, West Europe)
    
* Username, Password
    
* Storage settings
    
* Network settings
    

You fill in all details and click **Create**.

Now what happens behind the scenes?

1. Your request goes through the internet to Microsoft Azure’s cloud control system.
    
2. Azure looks into its available data centers and finds a **physical server** that has enough free resources.
    
3. It picks a suitable host machine.
    
4. It launches the hypervisor on that server to **create a new virtual machine** for you.
    
5. That machine is given your requested configuration.
    
6. It is now connected to the internet, assigned a public IP, and ready for you to use.
    

You see a message: **“Deployment Successful”**  
And the virtual machine appears in your Azure portal dashboard.

Now, from anywhere in the world, you can:

* Connect to that VM
    
* Install software
    
* Host your website
    
* Use it like a real computer
    

### **Let’s Recap Everything Together:**

* A **data center** is a huge place filled with **physical servers**.
    
* Each server is converted into a **virtualization host** by installing a hypervisor (like Hyper-V).
    
* Using this hypervisor, **dozens or hundreds of virtual machines** are created on a single server.
    
* Each virtual machine is used by a **different customer** — for different needs.
    
* Customers don’t even know which physical machine is being used.
    
* The entire backend process is **automated, optimized, and invisible** to the user.
    
* The front-end (what the customer sees) is the **Azure portal**.
    
* The backend (what actually runs things) is the **physical data center** and hypervisor-managed servers.
    

### **A Real-World Analogy: How Cloud Uses Virtual Machines**

Just like someone can install VMware on their laptop to create virtual machines, cloud providers like Microsoft do something similar at a much larger scale. In their data centers, each physical server runs a hypervisor, which allows them to create hundreds of virtual machines on a single server.

The only difference is the hardware capacity. While a personal laptop might have 16GB of RAM, these servers often have 1024GB (or more) RAM, along with powerful CPUs and large storage.

Each virtual machine is assigned to a different customer and runs in a completely isolated environment. This isolation ensures security and performance. This setup forms the foundation of how cloud computing works behind the scenes.

**😮 But Wait – A Real Problem in Traditional Virtualization**

Until now, we’ve understood how virtualization works inside a data center — how one powerful physical server is converted into a virtualization host and runs many virtual machines (VMs) for different customers using a hypervisor.

But now let’s talk about a **problem** — a limitation that existed **before the cloud revolution** came in.

Let’s say a company is using a traditional virtualization setup. That means they’ve installed VMware ESXi (Type 1 hypervisor) on all their servers.

So now they have:

* Dozens or even hundreds of virtual machines
    
* All running on different physical hosts
    
* Spread across their internal data center
    

Sounds great so far, right?

But here’s the catch:

* These virtual machines are **not managed individually**
    
* Instead, all of them are managed using a **central control software** known as **vCenter Server**
    

### **🤔 What is vCenter Server?**

vCenter is like the **master control room** for all VMs created using VMware.

Think of it like:

* The brain of the whole virtual infrastructure
    
* A centralized interface where:
    
    * You can create new VMs
        
    * Monitor existing VMs
        
    * Assign resources
        
    * Delete or restart machines
        
    * Do all VM-related operations
        

In simple words:

“vCenter Server is the place from where you can manage the entire virtual data center.”

### **🚫 But Here Comes the Problem…**

Now imagine this:

You're working in an office, and your data center is either inside the same office building or maybe connected through the company’s internal network (LAN).

As long as you're inside the building or connected through VPN (Virtual Private Network), you can access vCenter and manage your virtual machines.

But the moment you leave the office — let’s say:

* You travel to **Kuwait**
    
* Or you’re working from home
    
* Or you're on a holiday in a different city
    

You suddenly realize:

❌ You cannot access vCenter from anywhere else!  
❌ You can’t open the vCenter dashboard  
❌ You can’t start or stop a VM  
❌ You are stuck!

Why?

Because **vCenter only works inside the company’s private network**. It is not built for the public internet. It is meant for **on-premise use**.

So now you’re helpless. You have the knowledge, but you can’t access your infrastructure.

## **And This Gave Birth to Cloud Portals!**

When Microsoft, Amazon, and other big players saw this problem, they thought:

“Why not build something that people can access from **anywhere in the world**?”

“Why not give users a **web-based interface** to manage their virtual machines, without being dependent on internal networks or VPNs?”

And this thought gave birth to what we now call the **Cloud Control Plane** or simply the **Cloud Portal**.

### **What Did Microsoft Do?**

Microsoft took the concept of virtualization + remote management and created a full-fledged web platform where users could:

* Login from anywhere
    
* Create virtual machines
    
* Manage storage, networks, firewalls
    
* Monitor usage and billing
    
* And never have to worry about internal networks or VPNs again
    

They named this portal:

🔗 [https://portal.azure.com](https://portal.azure.com)

This website became the **heart of Microsoft Azure's cloud offering**.  
From this portal, you can manage every aspect of your cloud infrastructure — just by logging in with your username and password.

## **Azure Portal Is Just Like Zomato**

Now let’s understand this with a simple, real-world example:

Think about the **Zomato** or **Swiggy** app.

Here’s what happens:

1. You open the app
    
2. You browse through different restaurants and food items
    
3. You place your order — say, **2 plates of Shahi Paneer** or **1 medium pizza**
    
4. The order request goes to the restaurant
    
5. The kitchen starts preparing your order
    
6. Once the food is ready, a delivery partner picks it up
    
7. The food is delivered to your address
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754503268215/c4f41e30-6206-4ce3-9937-8c0898b9d161.png align="center")

You enjoy your meal, but you never:

* Go to the kitchen
    
* See how the food was made
    
* Visit the restaurant physically
    

Everything just works smoothly in the background.

### **Now Replace Zomato with Azure**

This is exactly what **Azure Portal** does with **cloud virtual machines**:

1. You open the Azure Portal website
    
2. You **login** with your credentials
    
3. You click on **Create Virtual Machine**
    
4. You fill in details:
    
    * OS (Ubuntu, Windows, etc.)
        
    * Size (e.g., DS1 v2 – 2 vCPU, 8 GB RAM)
        
    * Region (e.g., Southeast Asia)
        
    * Username and password
        
5. You click **Create**
    

And what happens next?

* Azure sends your VM request to one of its **physical data centers**
    
* It finds a suitable physical host
    
* It launches the **hypervisor**
    
* The hypervisor creates a new **virtual machine** for you
    
* The machine is configured with everything you selected
    
* It is now ready to use
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754503635828/813664b8-6cbf-48e4-8c0c-6e9417d34928.png align="center")

And just like the pizza reaches your doorstep, this virtual machine appears on your Azure dashboard.

You don’t see the physical machine.  
You don’t know in which rack or which city your server is hosted.  
You just get a **ready-to-use VM** delivered to you through the internet.

## **Step-by-Step VM Creation Process in Azure**

Let’s go through the full flow in the order your instructor explained:

1. **Open the Portal**:  
    Go to [https://portal.azure.com](https://portal.azure.com)
    
2. **Login**:  
    Enter your Azure account credentials and sign in.
    
3. **Click “Create” → Virtual Machine**:  
    Choose the option to create a new VM.
    
4. **Fill Details**:
    
    * Enter the **VM Name** (e.g., deepak-vm)
        
    * Choose **Region** (e.g., Southeast Asia)
        
    * Select **Size** (e.g., DS1 v2 = small size VM)
        
    * Choose the **Operating System** (Windows/Linux)
        
    * Set **Username & Password** for admin access
        
5. **Click “Create”**:
    
    * Azure starts the deployment process
        
6. **Behind the Scenes**:
    
    * Azure picks a data center with available physical resources
        
    * It triggers a **hypervisor** to create a virtual machine
        
    * All configurations are applied
        
    * The machine is started
        
7. **Status is Shown on Screen**:
    
    * “Deployment in Progress”
        
    * “Initializing Resources”
        
    * “VM Created Successfully”
        
8. **VM Appears on Your Dashboard**:  
    You can now connect to your VM via public IP, install applications, and use it just like a real machine.
    

### **Zomato Order vs Azure VM Status**

Let’s relate Azure's VM deployment to a Zomato order status:

| Zomato Status | Azure Portal Status |
| --- | --- |
| Order received | Request received |
| Food is being prepared | Virtual machine is being configured |
| Packed and out for delivery | VM is being deployed |
| Delivered | VM created and ready to use |

You never see the cooking.  
You never see the real data center.  
But you get your service — hot and fresh!

## **Final Thought: Cloud Made Simple**

So this is the **main advantage of cloud portals** like Azure:

* You don’t need to be in the office
    
* You don’t need to connect to internal VPNs
    
* You don’t need to access vCenter or physical hardware
    
* All you need is **internet and a browser**
    
* You get full control of enterprise-grade virtual machines — from anywhere in the world
    

That’s the power of the **Azure Portal**, and that’s how cloud computing removed the biggest barrier of traditional virtualization.

---

### **💭 Let’s Think Again – What Is the Cloud?**

When you use Azure portal to create VMs that are hosted in some remote data center, and you access them using the internet — that whole process is called **Cloud Computing**.

"Cloud is someone else’s computer — presented to you as if it’s your own."

You don’t own any physical server, but you:

* Use it
    
* Pay for it
    
* Control it via the portal
    

---

### **Wrapping It All Up:**

* A **Physical Server** can only run one OS natively.
    
* With **Virtualization**, we break that limit using a **Hypervisor**.
    
* Hypervisors come in two types:
    
    * **Type 1**: For real cloud (Azure, AWS)
        
    * **Type 2**: For training (VMware Workstation)
        
* You create multiple **Virtual Machines** on one server.
    
* Cloud platforms give you a **web portal (control)** to manage everything.
    
* Microsoft Azure offers this at [`portal.azure.com`](http://portal.azure.com)
    
* Creating a VM is just like ordering pizza on Zomato.
    
* The entire model is **Cloud**.