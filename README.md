# ⚙️ Go HTTP/1.1 Server (Built from Scratch)

A minimal yet functional **HTTP/1.1 server** implemented from scratch in **Go**, using only the standard `net` package.
This project was built to understand the internals of HTTP and TCP, following **[RFC 9110](https://datatracker.ietf.org/doc/html/rfc9110)** (HTTP Semantics) and **[RFC 9112](https://datatracker.ietf.org/doc/html/rfc9112)** (HTTP/1.1).

---

## 🚀 Features

- 🔌 **Built using raw TCP sockets**
- ⚙️ **Compliant with HTTP/1.1 semantics**
- 🧵 **Concurrent client handling** using goroutines
- 📦 **Chunked Transfer Encoding** support (streamed responses)
- 🖼️ **Binary data support** — serves images, videos, etc.
- 📝 **Request parsing** and **response generation** from scratch
- 🗂️ Simple **static file serving**

---

## 🧠 Motivation

The goal of this project was to:
- Deeply understand how HTTP actually works under the hood
- Explore Go’s low-level networking capabilities (`net` package)
- Learn how HTTP messages are parsed, formatted, and transmitted over TCP

---

## ⚙️ How It Works

1. The server listens on a TCP port (default `:42069`)
2. Accepts incoming TCP connections
3. Spawns a **goroutine** per client connection
4. Parses:
   - Request line (`GET /index.html HTTP/1.1`)
   - Headers
   - Optional body
5. Sends a valid **HTTP/1.1 response**, using:
   - `Content-Length` (for known sizes)
   - or `Transfer-Encoding: chunked` (for streaming)
6. Supports **binary and text** responses
7. Closes the connection

---

## 📚 References

- [RFC 9110 – HTTP Semantics](https://datatracker.ietf.org/doc/html/rfc9110)
- [RFC 9112 – HTTP/1.1](https://datatracker.ietf.org/doc/html/rfc9112)
- [Go `net` package](https://pkg.go.dev/net)

---

## 🧑‍💻 Author

**Dibakar Ghosh**
🔗 [GitHub Profile](https://github.com/dibakarghosh03)
