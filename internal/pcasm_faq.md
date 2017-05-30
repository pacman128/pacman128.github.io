---
layout: page
title: PC Assembly FAQ
menu: pcasm
permalink: /internal/pcasm_faq/
---

<ol>
<li>Where is the <em>asm_io.inc</em> file referred to
in the tutorial?
<p>
It's not listed anywhere in the tutorial; however, it is in the source
zip files. The <em>asm_io</em> object file that <em>asm_io.inc</em>
requires is also in the source zip files.
</p>
</li>
<li>Why does the example code generate segmentation fault/coredumps 
    on RedHat 7.1?
<p>
Red Hat 7.1 includes an rpm for version 0.98.xx of NASM. However, this
is <em>not</em> a stable release! Get version 0.97 or a more recent
0.98 version and all will be fine.
</p>
</li>

<li>Can I use the examples with the Windows cygwin port of gcc?
<p>
The <a href="http://www.cygwin.com/">Cygwin</a> gcc compiler port
seems to use the same object file format as Microsoft's Visual C/C++
compiler. So the <a href="ms-ex.zip">Microsoft examples</a>
<em>should</em> work with the Cygwin compiler. One person has
confirmed that it does, but I have not installed the Cygwin compiler
to confirm this myself.
</p>
</li>

<li>Can I use the examples with the Windows MinGW port of gcc?
<p>
Yes, but it will take some work. Like Cygwin, you will need to use the 
<a href="ms-ex.zip">Microsoft examples</a> and use -f win32 when assembling
your code. However, NASM will by default create an object file with a .obj
extension. MinGW needs an extension of .o instead. So you can either rename
the files yourself or tell NASM to when it generates them. Example,
<pre >
nasm -f win32 -o file.o file.asm
</pre>
<p>
You can change lines 16 and 17 lines of the Makefile to be:
</p>
<pre>
.asm.obj:
	$(AS) $(ASFLAGS) -o $*.o $*.asm
</pre>
<p>
to fix it to automatically do this.
</p>

<li>How can I compile the example code as 32-bit on a 64-bit Linux OS?
  <p > Yes, the makefile for Linux should work for 64-bit Linux
  now. However, you will need to 32-bit C library support. On
  debian-based systems, the following should work:
<pre>
sudo apt-get install g++-multilib libc6-dev-i386
</pre>
  </p>
</li>


<li>Is something wrong with Figure&nbsp;1.1?
<p>
It seems that this figure was misleading. The figure shows 8 separate
one bit additions, not 2 4-bit ones. This is <em>hopefully</em>
fixed in the current edition.
</p>
</li>

<li>Does the tutorial cover structures or C++?
<p >
Yes, a new edition of the tutorial added a chapter covering these topics.
</p>
</li>

<li>Is the tutorial available as HTML?
<p>
Unfortunately not. It is written in <em>LaTeX</em>, but uses some packages that
the <em>latex2html</em> does not support. If I was starting today, I
would probably use <em>DocBook</em> which can output many different
formats. However, it would be a very difficult job to convert the
existing files to <em>DocBook</em> as it does not support some features I used
in <em>LaTeX</em>.
</p>
</li>


<li>Does the tutorial cover MMX or SSE instructions?

<p> No, it doesn't and probably never will. I don't
know how to use these newer instructions. I'm not a real assembly
programmer. The tutorial is meant to be an introduction to assembly
for C/C++ programmers like myself. I try to stress the ideas from
assembly that I use all the time in my C/C++ programming.  I do not
really see any great advantage to adding another chapter covering these
instructions. After finishing my tutorial, it shouldn't be too
difficult to learn how to use these newer instructions from other
sources.
</p> 
</li>



<li>Do you take unsolicited questions?
<p> Questions, comments and corrections about the
tutorial are welcome and I will reply as promptly as I can. Questions
on how to write your own OS, <em>etc.</em> will probably be ignored unless I
feel qualified on the subject and find the question interesting. Homework
questions will be ignored and get your e-mail address added to my block list!
</p>


</li>

<li>Can I translate your tutorial to another language?
<p>
Yes, you may. However, I have not had much luck with others making this offer.
After sending them the LaTeX source, I never hear from them again. To help
stem this problem, I am making the LaTeX source for the first chapter available.
If you are serious about translating my tutorial, download the file below and
translate the first chapter. Send me your work and I will then send you source
for the other chapters. 
</p>

<p>
<a href="/static/pcasm-chapter1.zip">Chapter 1 LaTeX source zip file</a> Read the <tt>README</tt>
file for instructions on getting started.
</p>
</li>

<li>What are some other resources for PC assembly on the net?
<ul>

<li><a href="http://sourceforge.net/projects/nasm/">NASM
SourceForge project pages</a></li>

<li><a href="http://www.linuxassembly.org/">www.linuxassembly.org</a></li>
<li><a href="http://rs1.szif.hu/~tomcat/win32/">win32NASM</a></li>
<li><a href="http://msdn.microsoft.com/vstudio/express/visualC/default.aspx">
Microsoft's free compiler download</a></li>
<li>
<a href="http://webster.cs.ucr.edu/">Randall Hyde's Art of Assembly Page</a></li>
<li>
<a href="http://www2.dgsys.com/~raymoon/x86faqs.html">x86 FAQ</a></li>
<li>
<a href="http://www.intel.com/products/processor/manuals/index.htm">Intel's
processor documentation</a>
</li>
</ul>


