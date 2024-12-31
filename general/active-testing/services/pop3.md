---
description: Footprinting and general commands for testing the POP3 service
---

# POP3

### Generic connection

```
telnet 10.10.149.41 110
Trying 10.10.149.41...
Connected to 10.10.149.41.
Escape character is '^]'.
+OK [XCLIENT] Dovecot (Ubuntu) ready.
AUTH
+OK
PLAIN
.
USER linda
+OK
PASS Pa$$123
+OK Logged in.
STAT
+OK 4 2216
LIST
+OK 4 messages:
1 690
2 589
3 483
4 454
.
RETR 3
+OK 483 octets
Return-path: <user@client.thm>
Envelope-to: linda@server.thm
Delivery-date: Thu, 12 Sep 2024 20:09:54 +0000
Received: from [10.11.81.126] (helo=client.thm)
        by example.thm with smtp (Exim 4.95)
        (envelope-from <user@client.thm>)
        id 1soq7c-0007lW-PU
        for linda@server.thm;
        Thu, 12 Sep 2024 20:09:54 +0000
From: user@client.thm
To: linda@server.thm
Subject: Reading Books

Reading is a fundamental activity that offers numerous benefits across various aspects of life.
.
QUIT
+OK Logging out.
Connection closed by foreign host.

```
