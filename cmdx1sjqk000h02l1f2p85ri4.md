---
title: "Day1-Introduction To Cloud Computing"
seoTitle: "Virtualization & Hypervisors Explained | AZ-900 + AZ-104 Training"
seoDescription: "Start your AZ-900 + AZ-104 journey with an easy explanation of virtualization and hypervisors. Learn how this tech changed cloud computing forever."
datePublished: Mon Aug 04 2025 11:49:35 GMT+0000 (Coordinated Universal Time)
cuid: cmdx1sjqk000h02l1f2p85ri4
slug: day1-introduction-to-cloud-computing
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1754307417285/2a96ef47-8254-4873-9f19-e60ce1135933.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1754308013131/dfc9c6f1-2fcb-42c2-a91e-a0306ed9c380.png
tags: cloud, cloud-computing, virtualization, hypervisor, baremetal

---

## **Introduction to Pre-Cloud Infrastructure: The Old Way of Doing Business**

Before the concept of cloud came into existence, companies had to manage everything on their own, which involved setting up their own physical data centers. This means, if a company wanted to launch an application or service, they had to purchase hardware like servers, routers, storage devices, and hire IT staff to manage them.

For example, suppose a company invested **₹5 crores** to set up a data center. The cost doesn’t stop there. You have to pay monthly salaries to the staff who will manage the infrastructure, pay rent for the building or server room, and also pay electricity bills. All of this leads to **two types of expenses**:

* **Capital Expenditure (CapEx):** This is the one-time, initial investment done to set up the infrastructure. It includes buying servers, routers, storage devices, and setting up the building.
    
* **Operational Expenditure (OpEx):** These are recurring monthly expenses like electricity bills, maintenance, salaries, internet charges, etc.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754318968316/62ace5da-f37b-4afe-9601-e905c5fa7651.png align="center")

Because both CapEx and OpEx were high, only big companies could afford to start large-scale digital businesses. That is why startups were very rare in India during this time. But things started to change after cloud computing came into the picture.

### **A Real Business Story: Why Cloud Was Needed**

Let’s say **Tata** invested ₹5 crores to launch a mobile application called **Tata Neu**. They set up their own data center with:

* Servers
    
* Storage devices
    
* Networking devices
    
* A team of 50 employees
    

Every month, their operational cost came around **₹2–2.5 crores**. But after **6 months**, Tata realized the application wasn’t growing as expected. Their monthly revenue was only ₹5 lakhs. Imagine spending crores and not even earning enough to pay salaries!

Eventually, they decided to shut down. But here's the problem: What do they do with all the expensive hardware now? You can't sell enterprise-grade servers and routers on OLX like you sell furniture.

They thought, maybe they can rent the server space to others. But the old servers could only handle **one application at a time** (1:1 ratio). So renting it out wasn't possible. They needed a new approach.

## **The Breakthrough: One Server, Many Applications**

Before 2002, the biggest challenge in IT infrastructure was that a single physical server could run only one application. If a company wanted to run three different applications, they had to buy three different servers—even if those servers were being used at only 10% capacity.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754307888076/257ad02f-318d-4bf1-a0ad-7fa2a084c349.png align="center")

This led to enormous waste: unused processing power, unused memory, and wasted investment.

To solve this critical problem, around 2002 to 2004, a technology company introduced a **special software** that changed everything. It allowed a single physical server to run **multiple applications simultaneously**, without them interfering with one another.

This new solution laid the foundation for a concept that would completely revolutionize the IT industry.

That concept was called **Virtualization**.

## **What is Virtualization?**

### **Basic Idea:**

Virtualization is a special **technology** or **process** that allows us to take one physical computer (usually a powerful server) and divide it into **multiple smaller, independent computers**—which are not real physical machines but behave **just like real ones**.

Or

**Virtualization** is a **technology or technique** of **splitting a single physical resource** (like a server, computer, or hardware) into **multiple logical (virtual) resources**, each behaving like a **real and independent machine**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306254205/bd96f802-ebd0-4e93-b1af-20f0fd224389.png align="center")

These “smaller computers” are called **Virtual Machines (VMs)** or **Virtual Servers**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306322404/5b054454-b940-40e7-a70e-da722a7fca50.png align="center")

### **Imagine This Scenario:**

Let’s say you own a **very powerful computer** with a lot of memory (RAM), a strong processor (CPU), and large storage (hard disk).

Normally, you’d install one operating system on it—like Windows or Linux—and run your programs on that single system.

But with **virtualization**, you can:

* Install a **virtualization software** first.
    
* Then **create multiple virtual computers** inside that one real computer.
    
* Each of those virtual computers acts like a **separate physical machine**.
    

### **What Can Each Virtual Machine Do?**

Once you’ve created virtual machines using virtualization, each one of them:

**1\. Behaves Like a Real, Independent Computer**

Each virtual machine (VM) functions just like a normal desktop or laptop.

* It boots up like a real machine.
    
* You can log in, install software, browse the internet, run apps, etc.
    

From a user’s perspective, there is **no visible difference** between a virtual machine and a real physical one.

**2\. Can Have Its Own Operating System**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306392213/3cbf53aa-bf47-4282-bf42-46e9e9b494ad.png align="center")

* One VM can have **Windows 10** installed.
    
* Another VM can have **Linux Ubuntu**.
    
* A third can have **Windows Server 2019**.
    

Even though they all run inside the same physical machine, they can each use **different operating systems**, just like separate computers.

**3\. Can Run Its Own Set of Applications**

Each VM can have:

* Its own MS Office,
    
* Its own Zoom,
    
* Its own programming tools,
    
* Its own database server, and so on.
    

And all these applications **run independently** inside their own VM.

**4\. Can Be Restarted or Shut Down Independently**

* You can shut down **Virtual Machine 1**, while **Virtual Machine 2** keeps working.
    
* You can restart one, update one, or even delete one—**without disturbing the others**.
    

This means they are completely **isolated from each other**, even though they’re using the same physical resources.

### **How Is This Even Possible?**

Let’s say you have:

* 128 GB of RAM,
    
* 12 CPU cores,
    
* 2 TB of storage.
    

Using **virtualization software**, you can divide this powerful server into smaller units like:

* VM 1: 24 GB RAM, 4 CPU cores, 500 GB storage
    
* VM 2: 50 GB RAM, 6 CPU cores, 800 GB storage
    
* VM 3: 20 GB RAM, 2 CPU cores, 300 GB storage
    

Each of these VMs works separately, as if it's a real computer. You can assign them for different purposes, different users, or even different companies.

### **Real-World Analogy: Office Cubicles**

Here’s a very simple example to understand it better.

**Imagine:**

* You have a **large open office hall**.
    
* Instead of having one person use the entire room, you **divide it into cubicles**.
    
* Now, multiple employees can work in the same room, **without interfering with each other**.
    

Each cubicle:

* Has its own desk, chair, and computer.
    
* Is used by a different employee.
    
* Lets each person do their job independently.
    

They all:

* Share the **same room** (just like VMs share the same physical machine),
    
* But they work in **complete isolation**, without disturbing each other.
    

This is exactly how virtualization works:

* The **room** is the physical server.
    
* The **cubicles** are the virtual machines.
    
* The **employees** are the applications and operating systems running inside each VM.
    

### **Why Is This So Powerful?**

Before virtualization, if you wanted to run three applications, you had to buy **three physical servers**—which was costly and wasteful.

Now, with virtualization:

* You can buy **one powerful machine**,
    
* And **run multiple applications** on it using separate virtual machines.
    

This **saves money**, **uses resources better**, and gives **more flexibility**.

# **What is a Hypervisor? – The Engine Behind Virtualization**

Now that you know virtualization lets us run multiple virtual computers (called **virtual machines**) inside a single real computer (physical server), you might be wondering:

“But *how* does the computer do this?  
What enables one server to act like many small servers?”

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306439050/1888395f-3719-4a58-9126-91988dbe5210.png align="left")

The answer lies in a special software layer called the **Hypervisor**.

### **Definition of Hypervisor**

A **Hypervisor** is a piece of software — or in some cases, firmware — that is installed on a physical computer and is responsible for:

* Dividing the hardware (CPU, RAM, storage) into parts
    
* Creating multiple **virtual machines** using those parts
    
* Managing and monitoring all the virtual machines (VMs)
    
* Making sure each virtual machine stays isolated and independent
    
* Allowing these VMs to run different operating systems and applications, all at the same time
    

Without a hypervisor, **virtualization is not possible**.

You can think of the hypervisor as a **traffic controller** sitting in the middle of the system. It:

* Keeps an eye on the road (hardware)
    
* Directs which vehicle (virtual machine) goes where
    
* Makes sure everyone drives safely without colliding (interfering)
    

### **What Exactly Does a Hypervisor Do?**

Once installed, a hypervisor takes complete control of your physical machine. Here's what it does step-by-step:

1. **Monitors all the available hardware resources** — like how much RAM, CPU, and storage you have.
    
2. **Allocates portions of those resources to create virtual machines**. Each VM is like a computer inside your computer.
    
3. **Keeps each virtual machine separate from others**, even though they all live on the same server.
    
4. **Acts as a translator** between the virtual machines and the actual hardware. For example, if a VM wants to use 2 CPU cores, the hypervisor tells the physical CPU to handle that request.
    
5. **Protects virtual machines from crashing into each other**, so that if one VM fails or shuts down, the others keep working.
    

It’s the **core system** that manages virtualization behind the scenes.

# **Understanding Types of Hypervisors**

### **What is a Hypervisor (Quick Reminder Before Types)?**

Before we dive into the types of hypervisors, let’s first remember what a **hypervisor** actually is.

A **hypervisor** is a special kind of software (or sometimes firmware) that allows you to create and manage **virtual machines (VMs)** on a single physical computer.

Without a hypervisor, you cannot run multiple operating systems or multiple servers on one single machine. It’s the **core technology** that makes **virtualization** possible.

Now, let’s move to the main part: the two types of hypervisors.

## **Type 1 Hypervisor**

### **What is It?**

A **Type 1 Hypervisor** is a hypervisor that is installed **directly on the physical hardware**, even before any operating system (like Windows or Linux) is installed.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306570724/b00dc67b-b96a-4d72-b147-c4bc64085a34.png align="center")

You can think of this as the **foundation of the whole system**. Just like a house is built on a solid foundation, Type 1 hypervisor is the first layer of software that sits on the **bare metal hardware** of a server.

This is why it is often called a **Bare Metal Hypervisor**.

### **What Does It Do?**

Once installed, this hypervisor takes full control of the machine’s resources such as:

* CPU (Processor)
    
* RAM (Memory)
    
* Storage (Disk space)
    
* Network interface (LAN, Internet access)
    

It then allows you to **create multiple virtual machines (VMs)** on that hardware. Each virtual machine behaves just like an actual computer, and you can install different operating systems on each one.

### **Why Is It Called "Firmware"?**

Normally, **software** is something you install **after** your operating system is ready (like installing MS Word or Zoom on Windows).

But **firmware** is software that is installed **before** the operating system — it becomes part of the foundational system that the OS sits on.

Since the **Type 1 Hypervisor is installed before the OS**, we also refer to it as **firmware**.

### **How Does It Work?**

* Turn on the server → It boots directly into the **hypervisor**
    
* The hypervisor loads → Allows the admin to create virtual machines (VMs)
    
* Each VM is assigned a portion of hardware resources (like 8 GB RAM, 2 CPUs, 200 GB disk)
    
* You can install any OS inside each VM (Windows Server, Ubuntu, Red Hat, etc.)
    

All this happens **without any main OS like Windows sitting in between** — the hypervisor runs the show directly.

### **Real-World Analogy:**

Imagine you’re constructing a **brand-new house** on an empty plot of land.

Before adding any furniture or even walls, you need to:

* Lay the concrete foundation.
    
* Build the basic structure that will hold everything else.
    

That’s exactly what a **Type 1 hypervisor** is — it’s the **foundation** for the system.

Once the foundation is ready, you can:

* Build rooms (virtual machines),
    
* Paint walls (install OS),
    
* Add furniture (install apps).
    

### **Who Uses Type 1 Hypervisors?**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306619990/f6f278a3-ded4-4692-ae52-535e1303e475.png align="center")

Type 1 Hypervisors are used by:

* **Cloud service providers** like Microsoft Azure, Amazon AWS, Google Cloud
    
* **Big enterprises** running private cloud systems
    
* **Data centers** hosting websites, databases, and applications for multiple customers
    

They are known for:

* **High speed**
    
* **Efficient use of resources**
    
* **Strong security**
    
* **Stability and reliability**
    

### **Examples of Type 1 Hypervisors in Real Use:**

| Company/Platform | Hypervisor Used |
| --- | --- |
| **Microsoft Azure** | Hyper-V |
| **Amazon Web Services** | Xen (earlier), and now **Nitro** |
| **Google Cloud Platform** | KVM (Kernel-based Virtual Machine) |
| **VMware Cloud** | ESXi |

These hypervisors run millions of virtual machines worldwide and are used in professional, large-scale systems.

## **Type 2 Hypervisor**

### **What is It?**

A **Type 2 Hypervisor** is a hypervisor that is **installed after** the operating system (like Windows or Linux) has already been set up.

It works just like any regular software or application — like installing a game, browser, or MS Office. This is why it's often called a **Hosted Hypervisor** or **Software Hypervisor**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754306691156/6962f45b-de71-43b3-bba3-b9fb1091d90c.png align="center")

### **How Does It Work?**

1. You turn on your computer (which has Windows or Linux installed).
    
2. You install a hypervisor software like **VirtualBox** or **VMware Workstation** just like any other app.
    
3. You open the hypervisor and start creating virtual machines inside it.
    
4. You can install different operating systems inside each virtual machine and run them simultaneously.
    

But the hypervisor doesn’t talk directly to the hardware. It goes through the host OS, so it's a bit **slower** and **less efficient** than Type 1.

**Real-World Analogy:**

Imagine you already live in a **fully built house**.

Now you decide to install an **air conditioner**, **gaming console**, or a **dishwasher** — things you can add **after** the house is complete.

These additions are helpful, but they are **not part of the foundation**.

Similarly, **Type 2 hypervisor is not the base layer**. It’s installed after the system is already built, and **depends on the host OS** to function.

### **Who Uses Type 2 Hypervisors?**

Type 2 Hypervisors are mostly used by:

* **Students and learners** for understanding virtualization
    
* **Developers and testers** for testing applications on different operating systems
    
* **Trainers** teaching Linux or Windows server administration
    
* **Enthusiasts** who want to try out a new OS without formatting their PC
    

These hypervisors are NOT used in large-scale cloud platforms because they are:

* Slower
    
* Less secure
    
* Not designed for production use
    

### **Examples of Type 2 Hypervisors in Real Use:**

| Tool/Software | Description |
| --- | --- |
| **Oracle VirtualBox** | Free and open-source, very popular for learners |
| **VMware Workstation** | Paid, feature-rich, used by IT professionals |
| **Microsoft Hyper-V (Client)** | Available in Windows Pro and Enterprise editions |

You can run Linux inside Windows using VirtualBox, test multiple OS versions, or even try hacking labs — all on your personal laptop.

### **Key Differences: Type 1 vs. Type 2 Hypervisors**

| Feature | Type 1 (Bare Metal) | Type 2 (Hosted) |
| --- | --- | --- |
| Installation Location | Directly on hardware | On top of an already-installed OS |
| Requires OS before install? | No | Yes |
| Speed and Efficiency | Very fast and efficient | Slower, depends on host OS |
| Used in Cloud? | Yes — Azure, AWS, GCP, VMware | No — mainly for testing and learning |
| Called As | Firmware | Software |
| Real Use | Hosting thousands of VMs in data centers | Running 2–3 VMs on a personal laptop |

### **Easy Rule to Remember:**

| If Installed... | It’s Called... | Type |
| --- | --- | --- |
| Before the Operating System | **Firmware** | Type 1 |
| After the Operating System | **Software** | Type 2 |

### **Final Thoughts**

**Type 1 Hypervisor:**

* Think of it like the **foundation of a building**.
    
* It’s the first thing that comes into place.
    
* Used in **real-world clouds**, runs very fast and handles massive workloads.
    

**Type 2 Hypervisor:**

* Think of it like an **extra gadget** added inside your home.
    
* It needs your **house (OS) to exist first**.
    
* Useful for **learning**, **testing**, and **experimenting**, not for real production.
    

---