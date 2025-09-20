## 🌐 Internet Protocols

Internet Protocols (IPs) হলো সেই নিয়ম-কানুন বা standard গুলো যেগুলো দিয়ে কম্পিউটার, সার্ভার, এবং অন্যান্য ডিভাইস ইন্টারনেটে একে অপরের সাথে ডেটা আদান-প্রদান করে। এগুলো ছাড়া নেটওয়ার্কে যোগাযোগ সম্ভব নয়।

# 🌐 TCP Protocol

## 🔹 What is TCP?

TCP (Transmission Control Protocol) is a **communication protocol** that works with IP (Internet Protocol).
It breaks data into **packets** and makes sure they are delivered **reliably and in order**.

---

## 🔹 How TCP Works

1. **Connection (3-way handshake)** → Sender & Receiver connect first.
2. **Data Segmentation** → Big data split into packets.
3. **Reliable Delivery** → Lost packets are resent.
4. **Ordering** → Packets are arranged in the correct order.
5. **Connection Close** → Ends safely after transfer.

---

## 🔹 Why TCP is Widely Used?

- ✅ Reliable (no data loss)
- ✅ Ordered delivery
- ✅ Error checking
- ✅ Connection-oriented
- ✅ Standard protocol for the internet

---

## 🔹 Examples of TCP

- 🌍 Web Browsing → HTTP/HTTPS
- 📧 Email → SMTP, IMAP, POP3
- 📂 File Transfer → FTP, SFTP

---

## 🔹 TCP vs UDP

| Feature         | TCP                             | UDP                      |
| --------------- | ------------------------------- | ------------------------ |
| **Connection**  | Connection-oriented (handshake) | Connectionless           |
| **Reliability** | Reliable (resends lost data)    | Not reliable             |
| **Ordering**    | Maintains order                 | Order not guaranteed     |
| **Speed**       | Slower (extra checks)           | Faster (less overhead)   |
| **Use Cases**   | Web, Email, File Transfer       | Gaming, Streaming, Calls |

---

# 🔹 TCP 3-Way Handshake

Before sending data, TCP makes sure both client and server are **ready**.
It uses special control flags: **SYN** (synchronize) and **ACK** (acknowledge).

---

## 🛠 Steps

1. **SYN (Synchronize)**

   - Client → Server
   - Client says: _"I want to connect, here’s my sequence number."_

2. **SYN-ACK (Synchronize + Acknowledge)**

   - Server → Client
   - Server replies: _"Got your request, here’s my sequence number too."_

3. **ACK (Acknowledge)**
   - Client → Server
   - Client confirms: _"Received your sequence number, let’s start communication."_

✅ Now the connection is established, and data transfer begins.

---

## 🔹 Visual Diagram

Client Server
| ----- SYN ----------------------> |
| |
| <---- SYN + ACK ----------------- |
| |
| ----- ACK ----------------------> |

---

## ✅ Why Needed?

- Ensures **both sides are ready** before communication.
- Prevents sending data to a server that isn’t prepared.
- Provides **reliability** that UDP doesn’t have.

---

# 🔹 UDP (User Datagram Protocol)

## 🛠 What is UDP?

UDP is a **connectionless communication protocol** that works with IP (like TCP/IP).
It sends data as **datagrams (packets)** without creating a handshake or guaranteeing delivery.

---

## 🔹 Why UDP is Fast?

- ❌ **No Handshake** → Sends data directly (no 3-way handshake like TCP).
- ❌ **No Reliability Check** → Doesn’t resend lost packets.
- ❌ **No Ordering** → Packets may arrive out of order, but that’s okay for speed.
- ✅ **Low Overhead** → Less processing, more speed.

---

## 🔹 When is UDP Used?

UDP is used when **speed matters more than reliability**:

- 🎮 Online Gaming (lag is worse than small packet loss)
- 📺 Video/Audio Streaming (live broadcast, YouTube Live, Zoom)
- 📞 VoIP Calls (slight glitches better than delay)
- 📡 DNS Lookups (small, quick queries)

---

## 🔹 Comparison: TCP vs UDP

| Feature         | TCP                             | UDP                       |
| --------------- | ------------------------------- | ------------------------- |
| **Connection**  | Connection-oriented (handshake) | Connectionless (no setup) |
| **Reliability** | Reliable, resends lost data     | Unreliable, no resend     |
| **Ordering**    | Maintains order                 | No order guarantee        |
| **Speed**       | Slower (extra checks)           | Faster (no overhead)      |
| **Best For**    | Web, Email, File Transfer       | Gaming, Streaming, Calls  |

---
