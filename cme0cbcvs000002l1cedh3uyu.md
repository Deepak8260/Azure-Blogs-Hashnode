---
title: "IP Addressing & MAC Addressing"
seoTitle: "IP vs MAC Address: Key Differences Explained"
seoDescription: "IP and MAC addresses are essential for network communication, serving as physical and logical identifiers"
datePublished: Wed Aug 06 2025 19:07:28 GMT+0000 (Coordinated Universal Time)
cuid: cme0cbcvs000002l1cedh3uyu
slug: ip-addressing-and-mac-addressing
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1754507104670/f3707d17-d8cc-4f0d-8e15-67eef1ff04ee.png
tags: ipv4, mac-address, ipaddress, ipv5, octet, classful-addressing

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1754507122033/1b6dd368-76c4-4d51-b096-4ea28b3a66a1.png align="center")

Note: This blog is an extension to Cloud computing. If you missed the previous one, click [here](https://kdazureblogs.hashnode.dev/day2-what-is-cloud-computing-and-intro-to-ip-address)

## **📢 Let’s Begin with a Simple Idea:**

“To understand how any two machines — whether in your home or in Azure — communicate with each other, you first need to understand **addresses**. Just like you and I have addresses so people can reach us, computers have addresses so data can reach them.”

There are **two types of addresses** you must understand before you move ahead with cloud networking:

1. **MAC Address** (Media Access Control) → This is the **physical address**
    
2. **IP Address** (Internet Protocol) → This is the **logical address**
    

Both work together. You **need both** for a computer or VM to participate in any network, whether it's your home Wi-Fi or Azure cloud infrastructure.

Let’s dive deep.

## **🔒 MAC Address – The Physical Identity of Every Device**

The **MAC address** is often called the **hardware address** or **physical address**. It is a **unique identifier** that is burned into your network hardware — specifically, into the **NIC (Network Interface Card)**.

Every device that can connect to a network — whether it’s a laptop, mobile phone, smart TV, or even your washing machine (if it’s IoT-enabled) — has at least **one NIC**, and **each NIC has a unique MAC address**.

The MAC address is usually written in **12 hexadecimal characters** grouped in pairs, like:

00:1A:2B:3C:4D:5E

This number is like a permanent name tag for your device in the world of networking.

---

### **💡 Real-Life Analogy:**

“Think of a MAC address like your **fingerprint** — you are born with it. It’s unique to you. It’s not something you change every day.”

Just like your fingerprint is permanent, a MAC address **does not change** (unless you physically replace your NIC).

---

### **⚠️ Common Misconception: "One Computer = One MAC Address"**

Many people assume that a computer or device has only one MAC address — but that’s not true.

A single device can have **multiple MAC addresses**, depending on the number of network interfaces it has. For example, a laptop with both Wi-Fi and Ethernet capabilities will have one MAC address for the Wi-Fi adapter and a different one for the Ethernet port.

Each network interface — whether wired, wireless, or virtual — has its own unique MAC address. So, the total number of MAC addresses on a device depends on how many ways it can connect to a network.

Let’s break this down.

Imagine your laptop or desktop. You might have:

* A **Wi-Fi adapter** to connect wirelessly
    
* An **Ethernet/LAN port** to connect via cable
    
* A **Bluetooth** interface for short-range devices
    
* A **virtual adapter** (e.g., when using a VPN or virtualization software like VMware)
    

Each of these **has its own network interface**, and hence, **its own MAC address**.

So your one laptop might actually have 3–5 MAC addresses!

| Connection Type | MAC Address |
| --- | --- |
| Wi-Fi | `00:14:22:01:23:45` |
| Ethernet (RJ45) | `20:89:84:5C:9D:F0` |
| Bluetooth | `10:20:30:40:50:60` |
| Virtual Adapter | `DE:AD:BE:EF:CA:FE` |

So again:

“The **number of MAC addresses** your device has depends on **how many different ways** it can connect to the internet or a network.”

This is extremely important in real-life IT and cloud scenarios.

---

## **🌐 What is an IP Address? – Deepest Level of Understanding**

“A computer without an IP address is like a house without a name or number. You may live in it, but no one can find it, and you can’t send anything out from it.”

So to communicate in any network — whether it's a home network, office, or even in Microsoft Azure — your machine needs an address that makes it **uniquely identifiable** and reachable. This address is called the **IP address**, or **Internet Protocol address**.

### **🧭 IP = Logical Address**

The **IP address is a logical address**, meaning it's assigned by software and can be changed as needed. It's not hardcoded like the MAC address.

The **purpose of the IP address** is very clear:

* It is used to **identify** a device in a network.
    
* It is used to **communicate** with other devices.
    
* It is used to **route** data from one machine to another.
    

If there are **100 devices** in a room and only 99 have IP addresses, that **one device without an IP is isolated**, silent, untraceable, and essentially **useless in the network**.

“You can give it RAM, CPU, or even a powerful OS — but if it doesn’t have an IP, it’s dead to the network.”

This applies to:

* Your laptop
    
* Your mobile phone
    
* Your smart TV
    
* And even your **virtual machines on Azure**
    

## **🔢 Understanding IPv4 – The Most Common IP Version**

There are two versions of IP addresses:

1. IPv4 (Version 4)
    
2. IPv6 (Version 6)
    

But in most networks and in Azure, **IPv4** is still the most commonly used. So the instructor focused deeply on this version first.

### **📘 IPv4 Format – The 32-Bit Number**

The IPv4 address is a **32-bit** address. But because humans find it hard to read 32 binary digits, it is shown in a simpler format called **Dotted Decimal Notation**.

So a 32-bit IP address is shown like this:

192.168.1.1

Each group separated by a dot is called an **octet**, and it contains **8 bits**.

So:

* First octet: 192 → 8 bits
    
* Second: 168 → 8 bits
    
* Third: 1 → 8 bits
    
* Fourth: 1 → 8 bits
    

→ Total = 8 + 8 + 8 + 8 = **32 bits**

This is the format that everyone is familiar with when they open the command prompt and type `ipconfig`.

## **Range of Each Octet**

Each of the 4 octets can store any number from **0 to 255**, because 8 bits can represent 256 values.

So your full IPv4 address can range from:

0.0.0.0 to 255.255.255.255

But remember — **not all IP addresses are usable**. Some are reserved (we’ll see soon), and some are used for testing, broadcasting, or other special purposes.

## **Why Is Each Part Called an Octet?**

“The word *Octet* comes from the Greek root ‘octo’, which means **eight**. That’s why October used to be the 8th month in the old calendar. In IP addresses, each group has 8 bits — hence it is called an **octet**.”

This simple idea helps you remember:

"Each IP address = 4 octets = 32 bits."

## **IP Address Classification – What Are IP Classes?**

Not all IPs are created equal. Based on the **first octet**, IP addresses are divided into **five major classes** — each designed for a different type of network.

“A large company like Reliance may need lakhs of IPs. A small shop may need just 2. So IPs were divided into classes based on the size of the network they serve.”

Let’s understand these five classes:

### **All 5 Classes of IP Addresses**

| Class | First Octet Range | Who Uses It | Devices Per Network |
| --- | --- | --- | --- |
| A | 0 – 127 | Very large organizations | ~16 million |
| B | 128 – 191 | Medium-sized companies | ~65,000 |
| C | 192 – 223 | Small companies / homes | 254 |
| D | 224 – 239 | Multicasting / IPTV | Not for device allocation |
| E | 240 – 255 | Experimental / R&D | Reserved only |

Each class offers a different **number of host addresses**.

### **❗ Important Notes:**

* **Class A** begins from 0 to 127 — but :
    
    * `0.x.x.x` is **reserved**
        
    * `127.x.x.x` is used for **loopback testing**
        

So **Class A usable range** is actually:

1.0.0.0 to 126.255.255.255

## **🔁 Loopback Address – Ping Yourself!**

“Want to test if your network card is working? Just talk to yourself — your own machine.”

Use the **loopback IP**:

127.0.0.1

This is called the [**localhost**](http://localhost) address.

Try this:

1. Open CMD (Command Prompt)
    
2. Type ping 127.0.0.1
    
3. Press Enter
    

You’ll see ping replies.  
This means your **network card is active** — you are talking to your own machine.

This trick is commonly used to **test internal connectivity**.

## **Binary and Decimal Representation**

Now comes the twist — **computers don’t understand decimals**. Internally, they only work in **binary** (0s and 1s).

So, while you see:

192.168.0.1

The computer sees:

11000000.10101000.00000000.00000001

Here's how:

* 192 → 11000000
    
* 168 → 10101000
    
* 0 → 00000000
    
* 1 → 00000001
    

# **The History of IP Addressing – A Story from the Beginning**

---

### **📍Why is it important to know the history?**

IP addresses are used everywhere — at home, in schools, in data centers, and in cloud platforms like Azure and AWS. Despite being such an essential part of our digital lives, very few people understand where this system originated.

Understanding the history behind IP addressing helps us appreciate its purpose and how it has shaped the internet we use today. Before depending on something for a lifetime, it’s valuable to know how and why it was created.

So, let’s take a quick journey into the past to see how IP addressing started and how it became the backbone of modern communication over the internet.

## **🕰️ Let’s Travel Back to the 1960s and 1970s**

Back then, **the internet didn’t exist**.

Yes — there was no Google, no websites, no YouTube, not even emails as we know them.

But scientists, researchers, and especially **military organizations** in the **United States** were trying to build a way for computers to **talk to each other**.

Their aim was to:

* **Send files** from one university to another
    
* **Communicate** between military computers
    
* Share information **even if one location was destroyed**
    

Why? Because this was the time of the **Cold War**, and the U.S. military wanted a network that would **continue to work even during war or disaster**.

So they funded a research project called **ARPANET**.

## **ARPANET – The First Internet**

ARPANET stands for:

**Advanced Research Projects Agency Network**

It was the **first successful packet-switching network**, and it is considered the **grandfather of the modern internet**.

This project was funded by an agency called **DARPA** (Defense Advanced Research Projects Agency), which was part of the U.S. Department of Defense.

### **But There Was One Big Problem…**

As more and more computers were being added to this early network, there was **no standard system** for identifying which computer was which.

Think about it:

* You have 10 computers.
    
* You want to send a message to computer #7.
    
* But how do you know which is #7?
    

There was **no concept of an IP address** at the time.  
They tried using host names and simple numbers, but it quickly became messy and unmanageable.

“Imagine 1000 computers in a network and no house numbers — chaos!”

So they needed a **standard way** to assign addresses to every computer — something that could:

* Identify each machine uniquely
    
* Help in sending and receiving messages
    
* Be understood by all systems
    

## **The Birth of IP Addressing (1981)**

Finally, after years of research, in the year **1981**, a formal document was published.

This document was called:

**RFC 791**

### **📖 What is an RFC?**

“RFC stands for **Request For Comments**. It’s a type of public technical document where internet engineers publish their ideas and standards.”

When an RFC becomes widely accepted, it becomes the **standard rule** for the internet.

So **RFC 791** was the official document that **introduced and defined IPv4** — the Internet Protocol version 4 — which is still the most used version of IP addressing today.

### **📘 What Did RFC 791 Contain?**

RFC 791 introduced:

* The **format** of IP addresses (32-bit, divided into 4 octets)
    
* The idea of **logical addressing**
    
* The use of IP addresses in **routing**
    
* The difference between **host** and **network**
    
* The need for **classes of IPs** (A, B, C, D, E)
    

This document laid the **blueprint** of how devices would talk to each other over the internet.

Even today, when we assign an IP like `192.168.0.1`, we are following the **rules written in RFC 791** back in 1981!

### **What Was India Doing at That Time?**

Back in 1981, while countries like the United States were developing the foundations of the internet — defining IP addresses and building early email systems — India was in a very different stage of technological growth. Color televisions were just becoming popular, and most universities had limited or no access to computers.

Although India joined the digital revolution later, it has since made remarkable progress. Today, the country is playing a major role in global technology and innovation.

This contrast highlights the long-term vision of the early internet pioneers. The systems they designed over 40 years ago are still powering the internet today — a true example of forward-thinking design.

## **Why IPv4 Still Works Today**

Now, here’s the amazing part — even though IPv4 was created in 1981, it is:

* Still in use today
    
* Still supported by every router, server, cloud platform
    
* Still fast enough and flexible enough for most networks
    

That’s the power of **designing a system ahead of its time**.

But as the number of devices grew (think billions of smartphones, IoT devices, cloud servers), the number of available IPv4 addresses started running out.

This led to the development of **IPv6**, which provides **340 undecillion addresses** (that’s a number with 36 zeros).

## **And What About IPv5?**

* A common question that comes up is: *Why was IPv5 skipped? Why did we go directly from IPv4 to IPv6?*
    
* The answer lies in the fact that IPv5 did exist, but it was never meant for public or large-scale use. It was developed as an experimental protocol designed specifically for streaming and real-time communication. However, it was never completed or standardized.
    
* More importantly, IPv5 did not address the growing problem of IP address exhaustion — one of the major reasons for developing a new protocol. As a result, IPv5 was eventually abandoned.
    
* That’s why the world moved forward with IPv6, which was built to handle the limitations of IPv4 and meet the future demands of the internet.
    

## **Summary of the History of IP**

| Timeline | Event |
| --- | --- |
| 1960s–70s | U.S. military and universities created **ARPANET**, the first internet-like network |
| 1981 | **DARPA** publishes **RFC 791**, introducing IPv4 |
| 1981–Now | IPv4 becomes the standard for all internet communication |
| Early 1990s | IPv5 is designed for multimedia, but dropped later |
| Late 1990s–2000s | IPv6 is developed to solve address shortages |
| Today | IPv4 is still widely used; IPv6 adoption is growing fast |

## **Why This Matters for Cloud and Azure?**

Everything in Azure (or AWS, or GCP) depends on **IP addresses**.

* When you create a virtual machine, Azure gives it an IP.
    
* When your app connects to a database, it needs the IP.
    
* When you SSH into a VM, you're using its IP.
    
* When you load a website hosted in Azure — again, you’re routing through IP addresses.
    

“Even though you're studying cloud, if you don’t understand IP, you're just pressing buttons — not actually learning how it all works.”