## 💡 Layer 5: Session Layer (OBJ 1.1)

The Session Layer (Layer 5) is responsible for establishing, maintaining, and tearing down sessions (conversations) between applications. A session keeps data separate to prevent intermingling or cross-contamination. Associate H.323, RTP, and NetBIOS with Layer 5.

✅ **Establishing a Session**
- Checks user credentials.
- Assigns a session number for identification.
- Negotiates services and determines who talks first.

✅ **Maintaining a Session**
- Transfers data back and forth.
- Reestablishes connection if broken.
- Acknowledges receipt of data.

✅ **Tearing Down a Session**
- Occurs when communication is complete (mutual agreement).
- Can also occur if one party disconnects or becomes unresponsive.

✅ **Layer 5 Protocols/Concepts**
- **H.323:** Used to set up, maintain, and tear down voice and video connections (e.g., FaceTime, Skype).
- **RTP (Real-time Transport Protocol):** Associated with streaming audio/video, often in two-way formats like phone calls.
- **NetBIOS:** Used by computers to share files over a network (e.g., Windows file sharing).