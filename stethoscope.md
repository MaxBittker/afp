# Talk Title

What Sound Does An Operating System Make? Let's Sonify System Calls!

# Abstract for your talk

Computers are too quiet, you can't tell what they're thinking!

Lets construct a digital stethoscope to amplify the inner workings of our computer, and see what we can hear!

I'll talk to you about system calls, sonification, and enriching our understanding of the world through our senses.

# Timeline for your talk

## Introduction, 2.5 minutes:

I want to open by talking about NPR show "Car Talk", where car problems are diagnosed over the phone via people making silly sounds with their mouth.

I'll connect this to old computers and the noises they made. Once, it was normal to debug your mainframe by ear!

I will pose some questions about the multi-sensory relationships humans have with machines and with the world.

"How can we listen to our computers today, and what do they sound like?"

## OS Concepts, 3 minutes:

To answer this question, I'll introduce a rough model of the structure of an operating system, and identify system calls as a "moving part" of that machinery that we should listen to!

I'll show the tool `strace` and how it can print system call events in real time. I'll demonstrate that those events react to normal computer tasks like copying a jpg.

## Design process & demo, 3 minutes:

Now that we have this raw stream of information, what should it actually sound like? Beeps? Saxophone solos? A screeching dial-up modem?

I'll discuss what considerations I took to design a sonification scheme that preserved information and sounded nice, while staying honest to the medium and material.

We'll do a fun demo, where I click around different programs on my desktop and we hear what sounds they make :)

## Conclusion: 1.5 minutes:

I want to end on a broader idea:
Our senses are powerful tools for communication and cognition.

Humans have many senses and emotions that get neglected by our goal-oriented computing tools.

"Strange translations" of an invisible system into a perceptible one allow us to relate to computers in enriching ways.

# Intended Audience

(Note: My demo is sound-based, and some of the points that I make will be through allusions to different sounds. I will try to avoid language that's unnecessarily alienating to people with hearing loss)

I want this talk to add new perspectives to the audience's existing relationship with computers. I won't expect people to already love systems programming or operating system theory!

When they leave they should have:

An understanding of what a "syscall" is, contextualized to everyday computing tasks and human time scales.

New questions about the computer as a system that can be observed and understood in unusual ways.
