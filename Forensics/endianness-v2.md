# Description
Here's a file that was recovered from a 32-bits system
that organized the bytes a weird way. We're not even
sure what type of file it is.
Download it here and see what you can get out of it

# Solution

By using CyberChef the file was put into the input section. Then converted to hex for the "Swap Endianness" function under a word length of 4. After this, the hex looks more like a JPG with the correct ÿØÿà␀␐JFIF␀␁ magic bytes start. After the endianness was swapped and save the file . and it automatically saved with the exension of jpg . open this image and you finally get the flag .

`Flag: picoCTF{cert!f1Ed_iNd!4n_s0rrY_3nDian_76e...}`

# ✅ Conclusion of the CTF:


### 🧠 What You Learned from This CTF Challenge:
#### 🔹 1. Understanding Endianness
Endianness is how multi-byte data is stored:

Big-endian: most significant byte first.

Little-endian: least significant byte first.

Swapping endianness is often required when transferring data between systems with different architectures.

#### 🔹 2. Architecture Matters
The mention of a 32-bit system was your clue to use a 4-byte word length.

Different architectures use different "word sizes" (e.g., 32-bit = 4 bytes, 64-bit = 8 bytes).

#### 🔹 3. File Signature Recognition
You learned how to recognize a JPEG file by its magic bytes:
FF D8 FF E0 (aka ÿØÿà in ASCII)

This helps identify file types even when filenames/extensions are removed or data is jumbled.


🏁 Final Takeaway:
Even when data looks broken or unreadable, understanding low-level data structures—like endianness and file signatures—can help you reconstruct and recover the original content.
