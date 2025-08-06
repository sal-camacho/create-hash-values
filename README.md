# Activity Overview
As a security analyst, you’ll need to implement security controls to protect organizations against a range of threats.

That’s where hashing comes in. Previously, you learned that a hash function is an algorithm that produces a code that can’t be decrypted. Hash functions are used to uniquely identify the contents of a file so that you can check whether it has been modified. This code provides a unique identifier known as a hash value or digest.

For example, a malicious program may mimic an original program. If one code line is different from the original program, it produces a different hash value. Security teams can then identify the malicious program and work to mitigate the risk.

Many tools are available to compare hashes for various scenarios. But for a security analyst it’s important to know how to manually compare hashes.

In this activity, we’ll create hash values for two files and use Linux commands to manually examine the differences.

## Scenario
In this scenario, I needed to investigate whether two files were identical or different. Although the contents appeared the same when viewed with `cat`, I used hashing techniques to verify their integrity.

Here’s how I completed the task:
- Explored the contents of the home directory and displayed both files
- Generated SHA-256 hashes for each file
- Saved the hashes to separate files
- Compared the hash files manually and with the `cmp` command

---

## Linux Cryptography — Create Hash Values
This report was completed as part of the Google Cybersecurity Certificate. It documents how to generate and compare hash values using Linux Bash commands. These tasks are essential for validating data integrity and detecting tampering in cybersecurity workflows.

## My Contributions
### Generate hashes for files
- Used `ls` to list files in the home directory
- Used `cat file1.txt` and `cat file2.txt` to display contents
- Used `sha256sum file1.txt` and `sha256sum file2.txt` to generate hashes

### Compare hashes
- Redirected hash outputs to new files using:
  ```bash
  sha256sum file1.txt >> file1hash
  sha256sum file2.txt >> file2hash

Tools Used
- ls — to list files
- cat — to read file contents
- sha256sum — to generate SHA-256 hash values
- cmp — to compare hash files byte by byte

Reflections
- Hashing revealed differences that were not visible in the file contents.
- Manual comparison of hash values reinforced the importance of integrity checks.
- This exercise demonstrated how even small changes in data produce entirely different hash values.
