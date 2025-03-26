Imagine a Register where each page contains notes about transactions. But there's a special twist:
Every page is linked to the previous one using a security code (hash).
If someone changes even a single word, the security codes break, revealing the tampering.

1. The Diary’s Structure (Blocks)
Each page in your diary contains:
A page number (index) – To keep track of the order.
A timestamp – When you wrote on that page.
The actual notes (data) – This could be "Alice sent 10 coins to Bob."
A special code (hash) – A unique security signature for this page.
A link to the previous page (previous hash)– Ensures the pages are connected.
If anyone tries to edit a past entry, the security code changes, and the diary recognizes the tampering.

2. How New Pages Are Added (Building the Blockchain)
When you add a new transaction, a new page is created:
It copies the last page’s security code.
It generates a new security code for itself.
It links to the last page, maintaining the chain.

3. The First Page (Genesis Block)
Every diary needs a first page. Since there’s no earlier page, it’s assigned a default value. This page is the foundation of the blockchain.

4. Keeping the Diary Secure (Validating the Blockchain)
Imagine someone tries to cheat by modifying a past transaction. The blockchain detects fraud using two rules:
The security code of each page must match its content.
If someone changes even one letter, the code changes completely.
Each page must correctly link to the previous page.
If someone removes or swaps pages, the links won’t match.
If either check fails, the blockchain knows someone tampered with the data!

5. Trying to Cheat (Tampering with the Blockchain)
Let’s say an attacker changes an old transaction (e.g., “Alice sent 10 coins” → “Alice sent 100 coins”):
The security code for that page changes.
The next page still expects the old code, creating a mismatch.
The blockchain immediately detects that something is wrong.
Even if the attacker tries to adjust all the codes, the process is computationally impossible in real blockchains.

6. Why This Matters
This system is a basic version of how cryptocurrencies like Bitcoin work:
-Transactions are secure and linked together.
-Fraudulent changes are easily detected.
-No single person can alter past transactions without breaking the chain.

output:
"C:\Program Files\Java\jdk-17\bin\java.exe" "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2024.3.4\lib\idea_rt.jar=60963" -Dfile.encoding=UTF-8 -classpath "C:\Users\Gobinath A\IdeaProjects\gobi\out\production\gobi" BlockchainDemo
Trying to tamper with the blockchain...
Blockchain after tampering:
Page Number: 0
Timestamp: 1742963648203
Content: Genesis Block
Previous Page Hash: 0
Security Code (Hash): 5282584265b4e21b7c5b7f8cd56a4f263feac735d6a1e95be78752db73650641

Page Number: 1
Timestamp: 1742963648244
Content: Transaction 1: Kumar -> Akash
Previous Page Hash: 5282584265b4e21b7c5b7f8cd56a4f263feac735d6a1e95be78752db73650641
Security Code (Hash): a2c2191c4d2322d61d1f1ceb010469ff71424d018b1fdf4a868925be51b560d2

Page Number: 2
Timestamp: 1742963648244
Content: Transaction 2: Akash -> Birla
Previous Page Hash: a2c2191c4d2322d61d1f1ceb010469ff71424d018b1fdf4a868925be51b560d2
Security Code (Hash): 203c00c7f02936c59b59a857454f5eb28a4b523428e216e13c3f5a9a35b45c3d

Page Number: 3
Timestamp: 1742963648247
Content: Tampered Transaction
Previous Page Hash: 203c00c7f02936c59b59a857454f5eb28a4b523428e216e13c3f5a9a35b45c3d
Security Code (Hash): bfcb3c075f68476b6e12086ce2083fac7d37bcd1cbefe221161054863be2075b

