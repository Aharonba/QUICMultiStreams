
# 🌐 QUIC Multi-Stream Protocol Simulation | Python

## 📌 Overview

A simplified simulation of the **QUIC (Quick UDP Internet Connections)** protocol built in Python, with support for multiple bidirectional streams over a single UDP connection. This project demonstrates core networking concepts such as **reliable data transfer**, **packet/frame abstraction**, **stream multiplexing**, and **asynchronous I/O** using `asyncio`.

---

## 🚀 Key Features

- **📦 QUIC-like Multi-Stream Support**  
  Simulates parallel data streams over a shared UDP socket, closely modeling the stream multiplexing behavior in QUIC.

- **⚙️ Asynchronous Programming**  
  Built with `asyncio` to handle concurrent sending and receiving of packets with minimal blocking.

- **🧩 Custom Frame & Packet Design**  
  Implements a flexible serialization format to structure stream frames, headers, and acknowledgments.

- **🔁 Flow Control & Reliability**  
  Supports data fragmentation, reassembly, acknowledgment handling, and delivery guarantees over UDP.

- **🔬 Testable Architecture**  
  A test suite simulates realistic scenarios of sender-receiver communication, including out-of-order packets and multi-stream interleaving.

---

## 🛠️ Technologies Used

- **Python 3.11+**
- **asyncio** – event loop and coroutines  
- **socket / UDP networking**  
- **Custom frame/packet protocol**  
- **Testing** – Manual test harness (`QUIC_TEST.py`)

---

## 📂 Project Structure

```
├── QUIC.py             → Core QUIC-like logic
├── sender.py           → Stream sender over UDP
├── receiver.py         → Stream receiver with frame tracking
├── QUIC_TEST.py        → Test harness for stream simulation
├── generate_data_file.py → Utility to generate data for tests
```

---

## 🧪 Example Usage

Run a receiver on one terminal:

```bash
python3 receiver.py
```

Send a multi-streamed file from another terminal:

```bash
python3 sender.py
```

Or run the main test simulation:

```bash
python3 QUIC_TEST.py
```

---

