# Motive

- programming technology has started repeating itself
- similar patterns appear in many languages and technologies
- what's needed now to make high-quality software is not
  tech, but education
- not "professionalism" or "better discipline" or "becoming
  a real engineering field"
- but recognition of our own limits (cognitive, emotional,
  biological) and the limits of our materials (code, hardware)
- the ability to communicate honestly and empathetically
  about what we are doing and why. No more plausible-sounding
  "reasons you can tell your boss" (I forget where this meme
  is from... some technical video I saw)

# What does the author get out of this book?

- A world of safer, simpler, more reliable software (I hope)
- The discovery of beautiful (i.e. self-harmonious,
  connected, humane) means to create truth (i.e. effective
  change, knowledge)
- And thus a unification of Christopher Alexander's _quality
  without a name_ and Robert M. Pirsig's _Quality_.

# What does the reader get out of this book?

The satisfaction that comes from creating effective systems
via beautiful means, aided by:

- An appreciation for three major software paradigms
  and knowledge of how to combine them effectively
- Knowledge of software patterns that recur over and over
  again, in many languages and paradigms
- An understanding of when and why to apply each pattern
  (and what to watch out for if you don't)
- A toolbox of ways to improve the development process
- Familiarity with a comprehensive philosophy of software
  development
- The ability to recognize and avoid rhetorical and
  intellectual traps to which software engineers are
  vulnerable
- The ability to better explain their own ineffable wisdom
  to junior engineers and nontechnical people.
- A list of references to high-quality, digestible resources

# What is a computer?

- A machine for automating mental toil that people do not
  want to do and are not very good at.
- programming is the process of describing one's mental
  model of the requisite toil to the computer in sufficiently
  precise terms that the computer can perform the task.
- The hardest part of programming is not getting something to
  work, but gaining the confidence that you have actually made
  something that works correctly in all the situations where it
  needs to. The need for confidence in our solutions
  is why we have tests, debuggers, type systems, IDEs,
  theorem provers, and all the other tools we use on a daily basis.
- If you are not the only person using the program, you may
  have to convey that confidence to other people in order for
  the program to be effective in the world. How you do this
  depends on the person. If they are technically-minded, you
  may be able to explain the logic behind your solution in
  some detail. If they are an end-user of your program, or
  a nontechnical coworker who has commissioned the program,
  a clear and consistent user experience, built from concepts that
  exist in the user's understanding of the domain, can
  foster confidence.


One implication of this description is that AI programming
should really be thought of as a separate class of programming.
So few of the confidence-building techniques listed above work
for AI. The only way to gain confidence in the system is to
look at how it performs. As such, AI programming is beyond
the scope of this book.

# Semantic Versioning

# Beware of Overgeneralization

# Name Things What They Are, Not How They're Used

# Separate Decisions From Dependencies

# Don't Mock What You Don't Own. Actually, Don't Mock What You Do Own. Screw It, Don't Use Test Doubles At All

# Deliberate Thought is Insanely Expensive and Not Very Effective

# Get Better at Typing and Examining the Assumptions Behind Quantitative Data

"How much gain can we get by teaching people to type 10 times faster? Not a lot, unfortunately." —@catswetel
https://www.youtube.com/watch?v=cW3yM-K2M08

Do we want to do the same old bad things faster? Or do we want
to do things better, and go faster that way?

I've worked with developers who were not fast typists. They are the developers who say things like:

- "we shouldn't write tests because it takes too long"
- "we shouldn't refactor this because it will take too long"

Poor editing ability adds a mental and emotional burden to
the most fundamental operation of programming: changing
code.

If you are focusing on just getting characters onto the
page, your attention is taken away from the higher-level
properties of your program.

When I was starting out at my first programming job, my boss
saw me clicking around with the mouse and recommended that I
get familiar with keyboard navigation shortcuts. That was
some of the best advice I ever received. I can try out
different approaches and explain them to my pair much more
quickly because I don't have to spend a lot of effort to get
my thoughts into a concrete form.

(Don't make a religion out of keyboard shortcuts, though. At
some point, the shortcuts become more of a distraction than
a help. **The goal is not to reduce the *time* taken, but to
reduce the amount of conscious thought you must put into
routine editing tasks.**)

We programmers often think of ourselves as logical people.
As such, we give a lot of credence to arguments (like Cat's)
backed up by quantitative data. But often we don't question
the assumptions that the use of that data entails.
Quantitative data never shows the whole picture. Use it with
caution.

## What is a Computer?

Our views of computers and software tend to be polarized into
two camps:

1. The computer is a brain-like machine that controls other
machines. It derives most of its behavior from
data—_programs_—that it retrieves from these other machines.
In this view, hardware is primary, and software is secondary.

2. A program describes a set of possible interactions
among actors in the world. A computer is the substrate that enables
programs to run—that is, it enables members of the set of possible
interactions to be manifest. In this view, the software is primary, and
hardware secondary.

Taken to extremes, both of these views are dehumanizing and ultimately
ineffective. Neither does a good job of supporting our understanding
of what programs are, what it means to run a program on a computer,
or how we should go about developing a computer system over time.

(A third view is to unify software and hardware into an "appliance".
Users think of the whole system as a machine with specific, fixed
behaviors.)

Recently, the second school of thought has prevailed.
Much effort has been spent in modern software design to hide from the
user the fact that they are interacting with a machine. The job of
the software engineer is to abstract away the underlying hardware
so thoroughly that the software seems to run by magic. But of course,
it isn't magic. When things go wrong, the user is confronted with
cryptic error messages or strange behavior, often because some engineer
forgot to consider a particular failure mode or sequence of interactions.
As Joel Spolsky put it, "all abstractions leak".

Problems compound when programs interact not with people,
but with other programs. Humans are generally okay at recovering even from
errors they don't understand; usually turning the computer off and on again
is enough to resolve the issue. Programs, however, are usually less tolerant
of errors and less able to recover. A system composed of such brittle,
error-intolerant programs is prone to failures that cascade through the system.
These failures are difficult for human operators to resolve because the
ultimate cause of the failure is often distant, both in time and in program-space,
from the symptom.

## The Ideal Computer System

From the programmer's perspective

- permits low-level manipulation of machinery without compromising security
- enables the creation of convenience wrappers that give the programmer
  greater leverage without concealing the underlying mechanism.
- enables computation to be expressed as pure functions where possible.

From the user's perspective

- is reliable
- is easy to use

## Aspects to Consider When Choosing Among Program Structures

- mean time between failures
- mean time to recovery
- maybe other failure metrics (99%ile time to recovery?)
- debuggability
- can code be safely reused for interactive debugging/recovery sessions in a production environment?
- test isolation and reproducibility
- interface stability: can the interface be extended without breaking clients?
- coupling
- cohesion
- can engineers quickly and accurately answer questions about the software by
  looking at the code? (TODO: what questions?)
- security

## Von Neumann Architectures

While contemplating the ASCII character chart, I was suddenly struck by
the realization that there is no such thing as inert "data". There are
only programs.

A huge subset of the ASCII codes represent not printable characters,
but instructions for a printer. The first 32 codes are not things a layperson
would consider "characters" in English or other languages by any stretch.

```
0  null
1  start of heading
2  start of text
3  end of text
4  end of transmission
5  enquiry
6  acknowledge
7  bell
8  backspace
9  horizontal tab
10 new line
11 vertical tab
12 form feed
13 carriage return
14 shift out
15 shift in
16 data link escape
17 device control 1
18 device control 2
19 device control 3
20 device control 4
21 negative acknowledge
22 synchronous idle
23 end of transmission block
24 cancel
25 end of medium
26 substitute
27 escape
28 file separator
29 group separator
30 record separator
31 unit separator
```

The fact that these codes come first in the ASCII "language" make the
purpose of ASCII clear: it is a language for controlling machines that
deal with text.

Seen from that perspective, the printable characters are no different
from the non-printable ones. They are instructions that tell a machine
to print (or store) a character. They are code; maybe not for *our*
processor, but certainly for someone else's.

## For Users

If you don't understand why things work when they work, you won't be
able to fix them when they don't.

Programmers are also users.

## The properties of a nice computer system

- The computer's effects on the other machines it controls are the
  transparent and predictable consequence of my (the user's) actions.
- The computer's effects flow smoothly from my desires as a human,
  not from arbitrary things that the computer "wants" me to do.
- I can see and understand what the computer is going to do before
  it does it.
- When something fails, it fails because of an obvious and natural
  constraint of the hardware or other resource.
- Failures are surfaced to the user in an honest and transparent way.
- Failures have an obvious fix. The "right" fix may be a little more
  work.
- The user can work most effectively by interacting with all levels
  of abstraction in about equal proportions. As a result, users are
  comfortable dropping down to the lowest level of abstraction when
  required to fix problems.
- The lowest level of abstraction is a comfortable place to work.
- Every single part is simple. Their aggregate is also simple.
- Names are pronounceable. Humans communicate by talking.

### Software

- There are standard UI components that make sense for >90% of
  cases.
- The operating system makes it easy for software to use the standard
  components, but does not require it.
- GUIs incorporate plain text. Console-type UIs may incorporate graphics.
- All software has a programmatic interface.
