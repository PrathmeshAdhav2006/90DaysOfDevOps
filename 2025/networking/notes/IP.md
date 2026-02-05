# 🌐 IP Addressing – IPv4, IPv6, and Subnetting

---

## 📌 Introduction to IP Address

An IP Address (Internet Protocol Address) is a unique number given to each device connected to a network.

It helps in:

- Identifying devices  
- Sending and receiving data  
- Locating destination systems  

Example:
192.168.1.1



Without IP addresses, communication on the Internet is not possible.

---

# 🌍 Types of IP Addresses

There are two main types:

1. IPv4 (Internet Protocol Version 4)  
2. IPv6 (Internet Protocol Version 6)  

---

# 📘 IPv4 (Internet Protocol Version 4)

## 📌 Introduction

IPv4 is the most widely used IP addressing system.

It uses 32-bit addresses written in decimal format.

---

## 📍 Format of IPv4

IPv4 has four parts (octets) separated by dots.

Example:

192.168.10.25




Each part ranges from 0 to 255.

---

## 📊 Size of IPv4

- 32 bits long  
- Total addresses ≈ 4.3 Billion (2³²)

---

## 📚 Classes of IPv4

IPv4 is divided into five classes:

| Class | Range               | Use            |
|-------|---------------------|----------------|
| A     | 1.0.0.0 – 126.0.0.0  | Large networks |
| B     | 128.0.0.0 – 191.0.0.0| Medium networks|
| C     | 192.0.0.0 – 223.0.0.0| Small networks |
| D     | 224.0.0.0 – 239.0.0.0| Multicast      |
| E     | 240.0.0.0 – 255.0.0.0| Research       |

---

## ✅ Advantages of IPv4

- Simple to use  
- Widely supported  
- Easy configuration  
- Compatible with old devices  

---

## ❌ Limitations of IPv4

1. Limited Address Space  
   Only 4.3 billion addresses available.

2. Address Exhaustion  
   Due to mobiles, laptops, IoT, addresses are running out.

3. Less Security  
   No built-in encryption.

4. Manual Configuration  
   Needs DHCP or manual setup.

5. Not Future Proof  
   Cannot support unlimited devices.

---

# 🌍 IPv6 (Internet Protocol Version 6)

## 📌 Introduction

IPv6 is the newer version designed to replace IPv4.

It solves the address shortage problem.

It uses 128-bit addresses.

---

## 📍 Format of IPv6

IPv6 is written in hexadecimal and separated by colons.

Example:
2001:0db8:85a3:0000:0000:8a2e:0370:7334


Short form:
2001:db8::8a2e:370:7334




---

## 📊 Size of IPv6

- 128 bits long  
- Total addresses ≈ 3.4 × 10³⁸ (Very Large)

Practically unlimited.

---

## ✅ Advantages of IPv6

- Huge address space  
- Built-in security (IPsec)  
- Faster routing  
- Auto-configuration  
- Better support for IoT  

---

## ❌ Limitations of IPv6

- Complex format  
- Not supported by old devices  
- Requires new infrastructure  
- Slow adoption  

---

# 🔄 Comparison: IPv4 vs IPv6

| Feature      | IPv4           | IPv6              |
|--------------|----------------|-------------------|
| Address Size | 32 bit         | 128 bit           |
| Format       | Decimal        | Hexadecimal       |
| Addresses    | Limited        | Unlimited         |
| Security     | Low            | High              |
| Speed        | Slower         | Faster            |
| Support      | Old + New      | Mostly New        |

---

# 🧩 How We Overcome IPv4 Limitation

Main Problem of IPv4:
Limited IP Addresses




Solutions:

1. NAT (Network Address Translation)  
2. Subnetting  
3. IPv6 Implementation  

In this chapter, we focus on Subnetting.

---

# 🌐 Subnetting

## 📌 What Is Subnetting?

Subnetting is the process of dividing a large network into smaller networks.

These smaller networks are called Subnets.

---

## ✅ Why Subnetting Is Used

Subnetting is used to:

- Save IP addresses  
- Reduce network traffic  
- Improve performance  
- Increase security  
- Manage networks easily  

---

## 📍 Example Without Subnetting

One big network:
192.168.1.0/24



All devices are in same network → More traffic.

---

## 📍 Example With Subnetting

Divided into two subnets:

192.168.1.0/25
192.168.1.128/25



Now traffic is reduced.

---

# 📘 Subnet Mask

## 📌 What Is Subnet Mask?

A Subnet Mask separates:

- Network part  
- Host part  

Example:
255.255.255.0




---

## 📍 Common Subnet Masks

| CIDR | Subnet Mask       | Hosts |
|------|-------------------|-------|
| /24  | 255.255.255.0     | 254   |
| /25  | 255.255.255.128   | 126   |
| /26  | 255.255.255.192   | 62    |
| /27  | 255.255.255.224   | 30    |
| /28  | 255.255.255.240   | 14    |

---

# 🧮 Subnetting Example

Given Network:
192.168.10.0/24



Need: 4 subnets

Step 1: Borrow 2 bits (2² = 4)

New CIDR:
/26




Step 2: New Subnets

192.168.10.0/26
192.168.10.64/26
192.168.10.128/26
192.168.10.192/26




Each subnet has 62 hosts.

---

# 🌟 Advantages of Subnetting

- Saves IP addresses  
- Better network control  
- Less congestion  
- Improved security  
- Easy troubleshooting  

---

# ❌ Disadvantages of Subnetting

- Complex calculation  
- Requires planning  
- Misconfiguration risk  

---

# 🧠 Simple Explanation

Think of IP network like a building:

- IPv4 = Small building  
- IPv6 = Big city  
- Subnetting = Dividing building into rooms  

Each room = One subnet

---

# ⭐ Final Summary

- IP Address identifies devices  
- IPv4 = Old, limited addresses  
- IPv6 = New, unlimited addresses  
- IPv4 problem = Address shortage  
- Subnetting helps save IPs  
- Subnet divides network into parts  

IPv6 + Subnetting together help in managing modern networks efficiently.




# 🌐 0.0.0.0 in Networking – Complete Explanation

---

## 📌 What Is 0.0.0.0?

0.0.0.0 is a special IP address in IPv4 that means:

> "No specific address" or "Unknown address"

It is not given to any real device.

It is used internally by computers and networks for special purposes.

---

## ✅ Main Meanings of 0.0.0.0

The meaning of 0.0.0.0 depends on where it is used.

It has three main uses:

1. Default Route  
2. No Address Assigned  
3. Listening on All Addresses  

---

# 1️⃣ 0.0.0.0 as Default Route

## 📌 Meaning

When used in routing tables, 0.0.0.0 means:

> "Send data to any unknown destination through this route"

It is called the **Default Route**.

---

## 📍 Example

In router:

0.0.0.0/0 → Gateway




Meaning:

All traffic that has no specific route goes through this gateway.

---

## 🧠 Simple Explanation

If the router does not know where to send data,
it sends it to the default route (0.0.0.0).

Like:

"If no road is found, take this highway."

---

# 2️⃣ 0.0.0.0 Means "No IP Assigned"

## 📌 Meaning

When a device starts and does not yet have an IP address,
it uses 0.0.0.0 temporarily.

It means:

> "I don’t have an IP address yet"

---

## 📍 Example

When your computer connects to Wi-Fi:

1. It first has 0.0.0.0  
2. It requests IP from DHCP  
3. Gets real IP like 192.168.1.10  

---

## 🧠 Simple Explanation

0.0.0.0 = "Waiting for IP"

---

# 3️⃣ 0.0.0.0 as "All IP Addresses" (Server Use)

## 📌 Meaning

In servers and applications, 0.0.0.0 means:

> "Listen on all available network interfaces"

It allows connections from any network.

---

## 📍 Example

In web server:

0.0.0.0:8080


Means:

Server accepts requests from all IPs on port 8080.

---

## 🧠 Simple Explanation

0.0.0.0 = "Open for everyone"

---

# 📊 Comparison: 0.0.0.0 vs Other Special IPs

| Address     | Meaning                    |
|-------------|----------------------------|
| 0.0.0.0     | No address / All addresses |
| 127.0.0.1   | Localhost (My computer)    |
| 255.255.255.255 | Broadcast address     |
| 192.168.x.x | Private network            |

---

# ⚠️ Is 0.0.0.0 Dangerous?

### ❌ For Normal Users
No, it is not dangerous.
It is used automatically by system.

### ⚠️ For Servers
Using 0.0.0.0 may be risky if security is weak,
because it allows connections from anywhere.

---

# 🏠 Real-Life Example

## When You Connect to Wi-Fi

1. Laptop starts → IP = 0.0.0.0  
2. Sends DHCP request  
3. Router gives IP  
4. Laptop gets real IP  

---

## When You Run a Server

Server running on 0.0.0.0:3000



Means:

Anyone in the network can access it.

---

# 🧠 Easy Way to Remember

Think of 0.0.0.0 like this:

| Situation        | Meaning              |
|------------------|----------------------|
| No IP yet        | "I have nothing"     |
| Default route    | "Go anywhere"        |
| Server binding   | "Accept everyone"    |

---

# ⭐ Advantages of Using 0.0.0.0

- Helps in routing  
- Helps in IP assignment  
- Useful in server setup  
- Flexible network handling  

---

# ❌ Disadvantages

- Can cause security risk in servers  
- Cannot identify real device  
- Confusing for beginners  

---

# 📘 Final Summary

- 0.0.0.0 is a special IP address  
- It means "no specific address"  
- Used as default route  
- Used when device has no IP  
- Used by servers to listen on all IPs  

### In Simple Words:

0.0.0.0 = Nothing + Everything (depends on use)


It is a system-level address, not for normal device use.




# 🌐 Number of IPv4 Addresses and How They Are Decided

---

## 📌 How Many IPv4 Addresses Can Be Created?

IPv4 uses **32 bits** to create an IP address.

So, the total number of possible IPv4 addresses is:

2³² = 4,294,967,296


That is approximately:

👉 **4.3 Billion IPv4 Addresses**

---

## ✅ Why 32 Bits Are Used in IPv4?

An IPv4 address is made of:

- 4 parts (octets)
- Each part = 8 bits

So:

bits + 8 bits + 8 bits + 8 bits = 32 bits


Example:
192.168.1.1


Each number (192, 168, 1, 1) comes from 8 bits.

---

## 📊 How Is This Number Decided?

Each bit can have two values:



0 or 1



So:

- 1 bit = 2 possibilities  
- 32 bits = 2³² possibilities  

That is why:

Total IPv4 = 2³² = 4,294,967,296
