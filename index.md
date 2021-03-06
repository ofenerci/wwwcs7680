---
layout: home
title: CS7680 Programming Models for Distributed Computation
---

<div class="grey">Special Topics in Computer Systems:</div>
<div class="course-title">Programming Models for Distributed Computing</div>

Distributed systems are everywhere today; games on smartphones are distributed
as are popular web applications, and distributed batch and streaming computation
on massive datasets is commonplace in industry today. To support this growing
trend, much research in recent years has been devoted to the confluence of
programming models and distributed systems. In this special topics course, we'll
focus on that confluence, programming models for distributed computation,
studying key publications describing systems and languages that have shaped how
we build systems today, by improving reliability (fault tolerance), facilitating
reasoning (correct-by-construction systems), and enabling better performance
(reduced synchronization, in-memory computation). Some of these ideas have had a
major impact in industry, and in these cases we'll highlight their relevance to
building systems and applications today, while others have fallen short.

Topics we will cover include, promises, remote procedure calls, message-passing,
conflict-free replicated datatypes, large-scale batch computation à la
MapReduce/Hadoop and Spark, streaming computation, and where eventual
consistency meets language design, amongst others.

## Organization

The course is a research seminar that primarily focuses on reading and
discussing papers from the scientific literature, and working together as a
group to author (and publish online) a collection of articles surveying the
landscape of programming models for distributed computation.

Every 1-2 weeks will be dedicated to a specific topic or programming model. Each
topic is covered by a selection of papers. Each student will be responsible for
reading and summarizing a specific paper, and for preparing a short presentation
about the publication to the class. A group discussion will follow the
presentation of all publications, aimed at understanding the differences between
each approach presented.

As a final project, students will be expected to collaborate on authoring
comprehensive survey articles covering each topic, to be published online as a
book/collection of articles surveying the state of programming models for
distributed programming to be shared with the open source community. As part of
the final project, we will evaluate different programming models.

## Grades

You will be evaluated on:

- Your weekly research paper summaries (20%)
- Your semi-weekly paper presentations (15%)
- Participation in discussion (10%)
- One-time minuting of the group discussion (1hr)(5%)
- Your final project (50%)

<br>
<h2><i id="announcements" class="fa fa-bookmark"></i> Announcements</h2>
<ul id="blog-posts" class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }} &raquo;</span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<br/>
<h2><i id="schedule" class="fa fa-calendar"></i> Schedule</h2>

<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Topic</th>
      <th>Reading</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>9/8</strong></td>
      <td>Introduction</td>
      <td>
        <ul>
          <li><a href="{{ site.baseurl }}/pdfs/CS7680-intro-slides.pdf">Intro slides</a></li>
          <li><a href="http://book.mixu.net/distsys/intro.html">(Intro) Distributed Systems for Fun and Profit</a></li>
          <li><a href="http://www.rgoarchitects.com/Files/fallacies.pdf">Fallacies of Distributed Computing Explained</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=9759286599132405476&hl=en&as_sdt=0,22">A View of Cloud Computing</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>9/15</strong></td>
      <td>RPC</td>
      <td>
        <ul>
          <li><a href="https://scholar.google.com/scholar?cluster=4214160207827716030&hl=en&as_sdt=0,22">Implementing Remote Procedure Calls (1984)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=16390299333503470630&hl=en&as_sdt=0,22">A Distributed Object Model for the Java System (1996)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=17011909832902326140&hl=en&as_sdt=0,22">A Note on Distributed Computing (1994)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=12184308525775656698&hl=en&as_sdt=0,22">A Critique of the Remote Procedure Call Paradigm (1988)</a></li>
          <li><a href="http://steve.vinoski.net/pdf/IEEE-Convenience_Over_Correctness.pdf">Convenience Over Correctness (2008)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>9/22</strong></td>
      <td>Futures, promises</td>
      <td>
        <ul>
          <li><a href="https://scholar.google.com/scholar?cluster=1955556762785357880&hl=en&as_sdt=0,22">Multilisp: A language for concurrent symbolic computation (1985)</a></li>
          <li><a href="{{ site.baseurl }}/pdfs/liskov1988.pdf">Promises: linguistic support for efficient asynchronous procedure calls in distributed systems (1988)</a></li>
          <li><strong>Oz dataflow concurrency</strong>. Selected sections from the textbook <em>Concepts, Techniques, and Models of Computer Programming</em>. <br><strong>Sections to read:</strong> 1.11: Dataflow, 2.2: The single-assignment store, 4.93-4.95: Dataflow variables as communication channels ...etc.</li>
          <!-- http://lampwww.epfl.ch/~hmiller/scala2013/resources/pdfs/paper4.pdf -->
          <li><a href="https://scholar.google.com/scholar?cluster=14809811497832734817&hl=en&as_sdt=0,22">The F# asynchronous programming model (2011)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=14922225451262628725&hl=en&as_sdt=0,22">Your Server as a Function (2013)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>9/29</strong></td>
      <td>Message passing <br><a href="http://www.csc.kth.se/~phaller/">Guest: Prof. Philipp Haller</a></td>
      <td>
        <ul>
          <li><a href="{{ site.baseurl }}/pdfs/Concurrent-Object-Oriented-Programming.pdf">Concurrent Object-Oriented Programming (1990)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=14666648622069497741&hl=en&as_sdt=0,22">Concurrency among strangers (2005)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=12143957832676562816&hl=en&as_sdt=0,22">Scala actors: Unifying thread-based and event-based programming (2009)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=3661419197567070875&hl=en&as_sdt=0,22">Erlang (2010)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=8745667089860760093&hl=en&as_sdt=0,22">Orleans: cloud computing for everyone (2011)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>10/6</strong></td>
      <td><strong>No class</strong></td>
      <td> </td>
    </tr>
    <tr>
      <td><strong>10/13</strong></td>
      <td>Distributed Programming Languages</td>
      <td>
        <ul>
          <li><a href="https://scholar.google.com/scholar?cluster=11916375963622989104&hl=en&as_sdt=0,22">Distributed Programming in Argus (1988)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=11241841329610336715&hl=en&as_sdt=0,22">Distribution and Abstract Types in Emerald (1987)</a></li>
          <li><a href="{{ site.baseurl }}/pdfs/Linda-Alternative-to-Message-Passing.pdf">The Linda alternative to message-passing systems (1994)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=14924122120956391575&hl=en&as_sdt=0,22">Orca: A Language For Parallel Programming of Distributed Systems (1992)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=8035716316641808258&hl=en&as_sdt=0,22">Ambient-Oriented Programming in AmbientTalk (2006)</a></li>
          <!-- <li>E</li> -->
          <!-- <li>Erlang</li> -->
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>10/20</strong></td>
      <td>Consistency, CRDTs</td>
      <td>
        <ul>
          <li><a href="http://www.glassbeam.com/sites/all/themes/glassbeam/images/blog/10.1.1.67.6951.pdf">Brewer's conjecture and the feasibility of consistent, available, partition-tolerant web services (2002)</a></li>
          <li><a href="https://hal.inria.fr/inria-00609399/document">Conflict-free Replicated Data Types (2011)</a></li>
          <li><a href="https://hal.inria.fr/inria-00555588/document">A comprehensive study of Convergent and Commutative Replicated Data Types (2011)</a></li>
          <li><a href="https://www.researchgate.net/profile/Eric_Brewer3/publication/260584236_CAP_twelve_years_later_How_the_Rules_have_changed/links/56a1cf3808ae24f62702165f.pdf">CAP Twelve Years Later: How the "Rules" Have Changed (2012)</a></li>
          <li><a href="{{ site.baseurl }}/pdfs/Cloud-Types.pdf">Cloud Types for Eventual Consistency (2012)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>10/27</strong></td>
      <td>Languages &amp; Consistency<br>Guest: Chris Meiklejohn</td>
      <td>
        <ul>
          <li><a href="http://db.cs.berkeley.edu/papers/cidr11-bloom.pdf">Consistency Analysis in Bloom: a CALM and Collected Approach (2011)</a></li>
          <li><a href="http://db.cs.berkeley.edu/papers/UCB-lattice-tr.pdf">Logic and Lattices for Distributed Programming (2012)</a></li>
          <li><a href="http://www.bailis.org/papers/consistency-socc2013.pdf">Consistency Without Borders (2013)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=2826500853026939967&hl=en&as_sdt=0,22">Lasp: A language for distributed, coordination-free programming (2015)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>11/3</strong></td>
      <td>Languages Extended for Distribution</td>
      <td>
        <ul>
          <li><a href="https://scholar.google.ch/scholar?cluster=8708455077175955066&hl=en&as_sdt=0,5">Towards Haskell in the Cloud (2011)</a></li>
          <li><a href="https://www.mpi-sws.org/~rossberg/papers/Rossberg,%20Le%20Botlan,%20Tack,%20Brunklaus,%20Smolka%20-%20Alice%20Through%20the%20Looking%20Glass.pdf">Alice Through the Looking Glass (2004)</a></li>
          <li><a href="http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.125.1527&rep=rep1&type=pdf">Concurrency Oriented Programming in Termite Scheme (2006)</a></li>
          <li><a href="https://scholar.google.ch/scholar?cluster=627024355240086822&hl=en&as_sdt=0,5">Type-safe distributed programming with ML5 (2007)</a></li>
          <li><strong>MBrace</strong>
            <ul>
              <li><a href="https://scholar.google.ch/scholar?cluster=2982751034759368856&hl=en&as_sdt=0,5">MBrace: cloud computing with monads (2013)</a></li>
              <li><a href="http://mbrace.io/programming-model.html">MBrace Programming Model (Tutorial)</a></li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>11/10</strong></td>
      <td>Large-scale, parallel processing (batch)</td>
      <td>
        <ul>
          <li><a href="http://jayurbain.com/msoe/cs4230/Readings/MapReduce%20-%20Simplified%20Data%20Processing%20on%20Large%20Clusters.pdf">MapReduce: simplified data processing on large clusters (2008)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=3662601067977846800&hl=en&as_sdt=0,22">DryadLINQ: A System for General-Purpose Distributed Data-Parallel Computing Using a High-Level Language (2008)</a></li>
          <li><a href="https://scholar.google.com/scholar?cluster=12651943154484674722&hl=en&as_sdt=0,22">Resilient distributed datasets: A fault-tolerant abstraction for in-memory cluster computing (2012)</a></li>
          <li><a href="https://cs.stanford.edu/~matei/papers/2015/sigmod_spark_sql.pdf">Spark SQL: Relational Data Processing in Spark (2015)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>11/17</strong></td>
      <td>Large-scale, parallel processing (batch)</td>
      <td>
        <ul>
          <li><a href="http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/35650.pdf">FlumeJava: Easy, Efficient Data-Parallel Pipelines (2010)</a></li>
          <li><a href="https://amplab.cs.berkeley.edu/wp-content/uploads/2013/05/grades-graphx_with_fonts.pdf">GraphX: A Resilient Distributed Graph System on Spark (2013)</a></li>
          <li><a href="http://www.vldb.org/pvldb/vldb2010/papers/R29.pdf">Dremel: Interactive Analysis of Web-Scale Datasets (2010)</a></li>
          <li><a href="http://www.dcs.bbk.ac.uk/~dell/teaching/cc/paper/sigmod08/p1099-olston.pdf">Pig latin: a not-so-foreign language for data processing (2008)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>11/24</strong></td>
      <td><strong>Thanksgiving holiday, no class</strong></td>
      <td> </td>
    </tr>
    <tr>
      <td><strong>12/1</strong></td>
      <td>Large-scale, streaming</td>
      <td>
        <ul>
          <li><a href="https://scholar.google.com/scholar?cluster=9379975392398657331">TelegraphCQ: continuous dataflow processing (2003)</a></li>
          <li><a href="https://cs.stanford.edu/~matei/courses/2015/6.S897/readings/naiad.pdf">Naiad: A Timely Dataflow System (2013)</a></li>
          <li><a href="https://www.usenix.org/system/files/conference/hotcloud12/hotcloud12-final28.pdf">Discretized Streams: An Efficient and Fault-Tolerant Model for Stream Processing on Large Clusters (2012)</a></li>
          <li><a href="https://cs.stanford.edu/~matei/courses/2015/6.S897/readings/google-dataflow.pdf">The Dataflow Model: A Practical Approach to Balancing Correctness, Latency, and Cost in Massive-Scale, Unbounded, Out-of-Order Data Processing (2015)</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>12/8</strong></td>
      <td>Final projects</td>
      <td><strong>One-on-one final project meetings throughout the week (no class)</strong></td>
    </tr>
  </tbody>
</table>
