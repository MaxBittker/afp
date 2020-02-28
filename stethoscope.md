# Talk Title

What Sound Does An Operating System Make?! Let's Sonify System Calls!

# Abstract for your talk

Computers are too quiet, you can't tell what they're thinking!

Lets construct a digital stethoscope, to amplify the inner workings of our computer and see what we can hear in there!

I'll talk to you about system calls, "sonification", and enriching our understanding of the world through our senses.

# Timeline for your talk

I want to open by talking about NPR show "Car Talk", where car problems are diagnosed over the phone via people making silly sounds with their mouth.

I'll connect this to old computers and the noises they made. Once, it was normal to debug your mainframe by ear!

I will pose some questions about the multi-sensory relationships humans have with machines and with the world.

"How can we listen to our computers today, and what do they sound like?"

To answer this question, I'll introduce a rough model of the structure of an operating system, and identify system calls as a "moving part" of that machinery that we should listen to!

I'll show the tool `strace` and how it can print system call events in real time. I'll demonstrate that those events react to normal computer tasks like copying a jpg.

Now that we have this raw stream of information, what should it actually sound like? Beeps? Saxophone solos? A screeching dial-up modem?

I'll discuss what considerations I took to design a sonification scheme that preserved information and sounded nice, while staying honest to the medium and material.

We'll do a fun demo, where I click around different programs on my desktop and we hear what sounds they make :)

Finally, I want to end on a broader idea:
Our senses are powerful tools for communication and cognition.

"Strange translations" of an invisible system into a perceptible one allow us to relate to computers in enriching ways.

Humans have many senses and emotions that don't get represented in our goal-oriented computing tools and that impoverishes our relationship to computers.

# Intended Audience

I this talk to provide new perspectives on the audience's existing relationship with computers. I won't expect people to already love systems programming or operating system theory!

When they leave they should have:

An understanding of what a "syscall" is, contextualized to everyday computing tasks at human time scales.

An appreciation for the computer as a system that can be observed from multiple levels. This should be interested to anyone interested in perception, cognition, and humans' relationships towards their tools and towards their senses!
