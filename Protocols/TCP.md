# What is TCP?

Imagine you have a big box of toy blocks, and you want to send them to your friend. But you can't send the whole box at once because it's too big. So, you decide to send the blocks one by one.

Every computer on the internet (or a local network) has an internet protocol address (IP Address) that uniquely identifies it. Within a server there may be multiple pieces of software running so how does a client know which one to connect to? Each service 'listens' on a particular port so that clients know where to connect.


## Sending Blocks

1. **Breaking Down the Box**: First, you take the big box and break it down into smaller pieces.
2. **Numbering the Blocks**: You put a number on each block so your friend knows the order.
3. **Sending the Blocks**: You send each block one by one to your friend.

## Receiving Blocks

1. **Getting the Blocks**: Your friend gets the blocks one by one.
2. **Checking the Numbers**: Your friend looks at the numbers to make sure they are in the right order.
3. **Putting the Box Together**: Your friend puts the blocks back together to make the big box again.

## Why is TCP Important?

TCP (Transmission Control Protocol) is like the way you send and receive the toy blocks. It helps computers send information in small pieces and makes sure everything arrives in the right order. This way, nothing gets lost, and everything works perfectly!

Some common port numbers:

Port|Service
-|-
80|HTTP (web)
443|HTTPS (secure web)
25|SMTP (email)
21|FTP (file transfer)
