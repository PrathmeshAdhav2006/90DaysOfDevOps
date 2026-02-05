# 🌐 Computer Networking – Basic Notes

## 📌 What Is Networking?

Networking is the process of connecting two or more devices (computers, mobiles, servers, printers, etc.) so that they can share data, resources, and services.

In simple words:

> Networking = Connecting devices to communicate and exchange information.

---

## ✅ Why Do We Need Networking?

Networking helps us to:

- Share files and data
- Access the Internet
- Share printers and hardware
- Communication (email, chat, video calls)
- Use shared servers and databases

Example:
- In a college lab, all computers are connected — this is a network.

---

## 🧩 Basic Components of Networking

### 1. Devices (Nodes)
Devices connected in a network:
- Computer
- Mobile
- Server
- Printer

### 2. Transmission Media
Medium through which data travels:
- Wired → Ethernet cable, Fiber
- Wireless → Wi-Fi, Bluetooth

### 3. Networking Devices
Special devices used to connect networks:
- Router
- Switch
- Hub
- Modem

### 4. Protocols
Rules for communication:
- TCP/IP
- HTTP
- FTP

They decide how data is sent and received.

---

## 📡 Types of Networks

### 1. LAN (Local Area Network)
- Covers small area (room, building, lab)
- Example: College computer lab

### 2. MAN (Metropolitan Area Network)
- Covers a city
- Example: City-wide network

### 3. WAN (Wide Area Network)
- Covers large area (country/world)
- Example: Internet

### 4. PAN (Personal Area Network)
- Covers very small area
- Example: Mobile and Bluetooth headset

---

## 💻 How Does Networking Work?

Example: Sending a file to a friend

1. Data is divided into packets
2. Packets travel through router/switch
3. Data moves via cable or Wi-Fi
4. Reaches destination device
5. Device reassembles data

This happens in milliseconds.

---

## 🏗️ Network Architecture

### 1. Client-Server Model
- One main server
- Other devices are clients
- Server controls data and services
- Example: Website hosting

### 2. Peer-to-Peer Model
- All devices are equal
- No central server
- Devices share data directly
- Example: File sharing

---

## 🔐 Advantages of Networking

- Fast communication
- Resource sharing
- Centralized data
- Easy backup
- Remote access

---

## ⚠️ Disadvantages of Networking

- Security risks
- Network failure affects many users
- Setup cost
- Requires maintenance

---

## 📘 Real-Life Examples

| Place   | Example |
|---------|----------|
| Home    | Wi-Fi for phones and laptops |
| College | Lab computers connected |
| Bank    | ATM connected to server |
| Office  | File sharing network |

---

Without networking, Internet and online services are not possible.

# 🌐 Tier 1, Tier 2, and Tier 3 Companies in Networking

The Internet works in three main levels called **Tiers**.  
Each tier has a different role in providing Internet service.

---

## 🥇 Tier 1 – Backbone Companies

### 📌 Role
Tier 1 companies build and own the main Internet infrastructure.

They spread Internet across countries and continents using fiber and submarine cables.

### ✅ Features
- Own global network
- Do not take Internet from anyone
- Connect with other Tier 1 networks
- Very expensive infrastructure

### 📍 Example Work
- Connecting countries and continents
- Handling international data traffic

---

## 🥈 Tier 2 – Regional Companies

### 📌 Role
Tier 2 companies take Internet on rent from Tier 1 companies and distribute it in large areas.

They act as middle-level providers.

### ✅ Features
- Buy bandwidth from Tier 1
- Cover countries, states, and big cities
- Sell Internet to Tier 3 companies
- Manage regional networks

### 📍 Example Work
- Providing Internet to cities
- Connecting different states

---

## 🥉 Tier 3 – Local Companies

### 📌 Role
Tier 3 companies take Internet from Tier 2 and provide it directly to users.

They install routers, cables, and give customer support.

### ✅ Features
- Serve homes, colleges, and offices
- Provide routers and Wi-Fi
- Handle local network problems
- Cheapest level

### 📍 Example Work
- Home broadband connection
- College and office Wi-Fi

---

## 🔁 Internet Flow

The Internet reaches users in this order:


---

## 📊 Comparison Table

| Tier   | Role              | Takes Internet From | Gives Internet To | Coverage Area |
|--------|-------------------|---------------------|-------------------|---------------|
| Tier 1 | Backbone Owner     | Nobody              | Tier 2            | Worldwide     |
| Tier 2 | Regional Provider  | Tier 1              | Tier 3            | Country/State |
| Tier 3 | Local ISP          | Tier 2              | Users             | Local Area    |

---

## 🧠 Easy Explanation

- Tier 1 → Makes Internet highways  
- Tier 2 → Connects cities  
- Tier 3 → Brings Internet to homes  

Like roads:


---

## ⭐ Real-Life Example

When you open a website at home:

1. Data comes from global servers (Tier 1)
2. Passes through regional networks (Tier 2)
3. Comes to local ISP (Tier 3)
4. Reaches your router
5. Comes to your device

This happens in milliseconds.

---

## 📘 Summary

- Tier 1 → Owns and spreads Internet worldwide
- Tier 2 → Rents from Tier 1 and distributes regionally
- Tier 3 → Gives routers and Internet to users

### Simple Formula


Without this system, Internet services would not reach users.


# 🌐 OSI Model (Open Systems Interconnection Model)

## 📌 Introduction

The OSI Model is a 7-layer reference model that explains how data is transferred from one device to another over a network.

It divides complex network communication into simple and manageable layers.

---

## ✅ Why OSI Model Is Needed

The OSI Model helps to:

- Understand how networks work  
- Design network systems  
- Troubleshoot network problems  
- Standardize communication  
- Divide work into layers  

---

## 🧱 Seven Layers of OSI Model

From top to bottom:

1. Application Layer  
2. Presentation Layer  
3. Session Layer  
4. Transport Layer  
5. Network Layer  
6. Data Link Layer  
7. Physical Layer  

### Memory Trick

**All People Seem To Need Data Processing**

---

# 📚 Explanation of Each Layer

---

## 1️⃣ Application Layer

### Function
- Provides interface between user and network  
- Allows users to access network services  

### Work
- Web browsing  
- Email  
- File transfer  
- Online chatting  

### Examples
- HTTP  
- FTP  
- SMTP  
- DNS  

---

## 2️⃣ Presentation Layer

### Function
- Translates data into readable format  
- Handles encryption and compression  

### Work
- Data formatting  
- Encryption and decryption  
- Compression  

### Examples
- Converting text to binary  
- Securing passwords  

---

## 3️⃣ Session Layer

### Function
- Creates, manages, and ends sessions  

### Work
- Start communication  
- Maintain connection  
- End connection  
- Recover sessions  

### Examples
- Video call session  
- Login session  

---

## 4️⃣ Transport Layer

### Function
- Provides reliable data transfer  
- Divides data into segments  

### Work
- Error control  
- Flow control  
- Retransmission  
- Port numbers  

### Protocols
- TCP (Reliable)  
- UDP (Fast, Not Reliable)  

---

## 5️⃣ Network Layer

### Function
- Finds best path for data  
- Handles logical addressing  

### Work
- Routing  
- IP addressing  
- Packet forwarding  

### Devices
- Router  

---

## 6️⃣ Data Link Layer

### Function
- Creates frames  
- Handles physical addressing  

### Work
- MAC address  
- Error detection  
- Frame synchronization  

### Devices
- Switch  
- Bridge  

---

## 7️⃣ Physical Layer

### Function
- Transmits raw bits (0s and 1s)  
- Manages physical connection  

### Work
- Cables  
- Voltage levels  
- Data speed  
- Connectors  

### Examples
- Ethernet cable  
- Fiber cable  
- Wi-Fi signals  

---

# 🔁 Working of OSI Model

## Sending Side (Encapsulation)

Data moves like this:

- Application → Presentation → Session → Transport → Network → Data Link → Physical  

Each layer adds its own information.

---

## Receiving Side (Decapsulation)

Data moves like this:

- Physical → Data Link → Network → Transport → Session → Presentation → Application  

Each layer removes information.

---

# 📦 Example: Opening a Website

When a user opens a website:

1. Application sends request  
2. Presentation encrypts data  
3. Session creates connection  
4. Transport divides data  
5. Network adds IP address  
6. Data Link adds MAC address  
7. Physical sends bits  

Reverse process happens at receiver side.

---

# 📊 OSI Model Summary Table

| Layer | Name         | Main Function          | Example |
|-------|--------------|------------------------|---------|
| 1     | Physical     | Bits, cables           | Wire    |
| 2     | Data Link    | MAC, framing           | Switch  |
| 3     | Network      | Routing, IP addressing | Router  |
| 4     | Transport    | Reliable delivery      | TCP     |
| 5     | Session      | Connection control     | Session |
| 6     | Presentation | Encryption, format     | SSL     |
| 7     | Application  | User interface         | HTTP    |

---

# ⚖️ Advantages of OSI Model

- Easy to understand  
- Standard structure  
- Easy troubleshooting  
- Modular design  
- Vendor independent  

---

# ❌ Limitations of OSI Model

- Complex structure  
- Mostly theoretical  
- Not directly implemented on Internet  

---

# 🌍 OSI Model in Real World

- OSI Model is a reference model  
- Internet mainly uses TCP/IP model  
- OSI is useful for learning and debugging  

--

Without the OSI Model, understanding network communication would be difficult.



# 🌐 TCP/IP Model (Transmission Control Protocol / Internet Protocol)

## 📌 Introduction

The TCP/IP Model is a practical networking model used for communication on the Internet.

It was developed by DARPA and is the foundation of modern Internet communication.

Unlike the OSI Model, the TCP/IP Model has four layers.

---

## ✅ Why TCP/IP Model Is Needed

The TCP/IP Model helps to:

- Enable communication between different networks  
- Support Internet data transfer  
- Provide reliable and fast communication  
- Standardize network protocols  
- Connect devices worldwide  

---

## 🧱 Layers of TCP/IP Model

The TCP/IP Model has four layers:

1. Application Layer  
2. Transport Layer  
3. Internet Layer  
4. Network Access Layer  

### Memory Trick

All Teachers In Need

---

# 📚 Explanation of Each Layer

---

## 1️⃣ Application Layer

### Function

- Provides network services to users  
- Combines OSI Application, Presentation, and Session layers  

### Work

- Web browsing  
- Email services  
- File transfer  
- Remote login  

### Protocols

- HTTP  
- HTTPS  
- FTP  
- SMTP  
- POP3  
- IMAP  
- DNS  

---

## 2️⃣ Transport Layer

### Function

- Provides end-to-end communication  
- Ensures data delivery between devices  

### Work

- Segmentation and reassembly  
- Error control  
- Flow control  
- Port addressing  

### Protocols

- TCP (Reliable, Connection-Oriented)  
- UDP (Fast, Connectionless)  

---

## 3️⃣ Internet Layer

### Function

- Handles logical addressing and routing  
- Selects best path for data transmission  

### Work

- IP addressing  
- Packet forwarding  
- Routing  

### Protocols

- IP (IPv4, IPv6)  
- ICMP  
- ARP  
- RARP  

---

## 4️⃣ Network Access Layer

### Function

- Handles physical transmission of data  
- Controls hardware communication  

### Work

- Framing  
- MAC addressing  
- Error detection  
- Data transmission  

### Examples

- Ethernet  
- Wi-Fi  
- Fiber  
- DSL  

---

# 🔁 Working of TCP/IP Model

## Sending Side

Data flows in this order:

- Application → Transport → Internet → Network Access  

Each layer adds its own header.

---

## Receiving Side

Data flows in this order:

- Network Access → Internet → Transport → Application  

Each layer removes its header.

---

# 📦 Example: Sending an Email

1. Application Layer creates email  
2. Transport Layer uses TCP for delivery  
3. Internet Layer adds IP address  
4. Network Access Layer sends data  

Receiver reverses this process.

---

# 📊 TCP/IP Model Summary Table

| Layer | Name           | Main Function             | Example Protocol |
|-------|----------------|---------------------------|------------------|
| 1     | Application    | User services             | HTTP, SMTP       |
| 2     | Transport      | Reliable delivery         | TCP, UDP         |
| 3     | Internet       | Routing and IP addressing | IP, ICMP         |
| 4     | Network Access | Hardware transmission     | Ethernet, Wi-Fi  |

---

# 🔄 OSI vs TCP/IP Comparison

| Feature     | OSI Model    | TCP/IP Model  |
|-------------|--------------|---------------|
| Layers      | 7            | 4             |
| Nature      | Theoretical  | Practical     |
| Usage       | Learning     | Internet      |
| Developed By| ISO          | DARPA         |

---

# ⚖️ Advantages of TCP/IP Model

- Used worldwide  
- Reliable communication  
- Scalable  
- Open standard  
- Supports multiple networks  

---

# ❌ Limitations of TCP/IP Model

- No clear separation of layers  
- Complex configuration  
- Security issues  




# 🌐 Router and Switch in Computer Networking

## 📌 Introduction

Router and Switch are important networking devices used to connect computers and networks.

They help in sending data from one device to another efficiently.

---

# 🔀 Switch

## 📌 What Is a Switch?

A Switch is a networking device that connects multiple devices within the same network (LAN).

It is mainly used inside homes, offices, and colleges.

---

## ✅ Why Switch Is Used

A Switch is used to:

- Connect computers in a local network  
- Send data to the correct device  
- Reduce network traffic  
- Improve network speed  
- Avoid data collision  

---

## ⚙️ Working of Switch

- A Switch works using **MAC addresses**
- It learns which device is connected to which port
- Sends data only to the intended device

Example:

If Computer A sends data to Computer B,  
the switch sends it only to Computer B.

---

## 📍 Features of Switch

- Works at Data Link Layer (Layer 2)
- Uses MAC address
- Works inside LAN
- Faster than Hub
- Secure communication

---

## 🏠 Example of Switch Use

- Connecting computers in a lab  
- Office internal network  
- College network  

---

# 🌍 Router

## 📌 What Is a Router?

A Router is a networking device that connects different networks together.

It connects a local network to the Internet.

---

## ✅ Why Router Is Used

A Router is used to:

- Connect LAN to Internet  
- Connect multiple networks  
- Choose best path for data  
- Provide Wi-Fi connection  
- Manage network traffic  

---

## ⚙️ Working of Router

- A Router works using **IP addresses**
- It checks destination IP address
- Selects best route
- Forwards data to next network

Example:

When you open a website,  
the router sends your request to the Internet.

---

## 📍 Features of Router

- Works at Network Layer (Layer 3)
- Uses IP address
- Connects different networks
- Provides Internet access
- Supports wireless connection

---

## 🏠 Example of Router Use

- Home Wi-Fi router  
- Office Internet connection  
- College Internet gateway  

---

# 📊 Difference Between Switch and Router

| Feature        | Switch                      | Router                     |
|----------------|-----------------------------|----------------------------|
| Purpose        | Connect devices in LAN      | Connect different networks |
| Works On       | MAC Address                 | IP Address                 |
| OSI Layer      | Layer 2                     | Layer 3                    |
| Internet       | Cannot provide Internet     | Provides Internet          |
| Area           | Local Network               | Wide Network               |
| Speed          | Very Fast                   | Slower than switch         |

---

# 🧠 Simple Explanation

- Switch → Connects devices inside a building  
- Router → Connects building to Internet  

Like roads:

Switch = Street Road
Router = Highway



---

# ⭐ Real-Life Example

In a house:

- All computers connect to Switch  
- Switch connects to Router  
- Router connects to Internet  

Flow:

Computer → Switch → Router → Internet





---

# 📘 Summary

- Switch connects devices in same network  
- Router connects different networks  
- Switch uses MAC address  
- Router uses IP address  
- Switch is for local communication  
- Router is for Internet access  

Both devices are essential for networking.

