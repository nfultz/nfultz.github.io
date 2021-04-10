SEMNET
======

### The Structural Equation Modeling Discussion Network

Researchers who study or apply structural equation modeling methods may be interested in an electronic mail network called SEMNET. Operating over the Internet, SEMNET is an open forum for ideas and questions about the methodology that includes analysis of covariance structures, path analysis, and confirmatory factor analysis. SEMNET bridges the gaps between users, between disciplines, and between conferences. SEMNET was founded in February 1993. As of November 1998, SEMNET had more than 1,500 subscribers around the world.

SEMNET is for sharing ideas about this methodology with other interested researchers. SEMNET is also for researchers who are just learning (or re-learning) about structural equation modeling, or who are facing problems in applying these techniques to their own research.

The current postmaster/list owner for SEMNET is Dr. Carl E. Ferguson, Jr. (CFERGUSO@ALSTON.CBA.UA.EDU), professor of marketing at The University of Alabama, in Tuscaloosa. SEMNET is sponsored by the Seebeck Computer Center at The University of Alabama.

### **TOPICS:**

-   [Commands vs. Messages](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Commands)-   [Addresses:](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Addresses)-   [Joining](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Joining) SEMNET-   Subscription [Options](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Options)-   [Leaving](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Leaving) SEMNET-   The [Archives](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Archives)-   [Searching](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Searching) the Archives-   For [More](https://web.archive.org/web/20190804223334/http://www2.gsu.edu/~mkteer/semnet.html#Moreinfo) Information . . .

### **COMMANDS VS. MESSAGES**

Interacting with SEMNET involves sending two different types of e-mail: **commands** and **messages**.\
Users send **commands** to acquire information about the list or to start, stop, or change the parameters of their subscription to the list. By contrast, users send **messages** to the list to be distributed to the list's other subscribers. For **commands**, users do not need to provide a subject. The commands themselves go in the body section of the e-mail. The same e-mail may contain several commands, but each command must be on a separate line.\
For **messages**, providing a descriptive subject line shows consideration for other list subscribers.

### **ADDRESSES**

SEMNET users need to remember two different e-mail addresses--one for **commands** and one for **messages**.\
**Commands** are always sent to the **LISTSERV** address:

`LISTSERV@BAMA.UA.EDU`

**Messages** are always sent to the **SEMNET** addresss:

`SEMNET@BAMA.UA.EDU`

Almost anything sent to the SEMNET address will be automatically distributed to all SEMNET subscribers around the world--so be careful. Be especially careful when writing a private reply to a SEMNET-distributed message, because you may find that your mailer has automatically inserted the SEMNET address as the "To" address.

### **JOINING SEMNET**

To join SEMNET, send the command:

`SUB SEMNET *first-name last-name*`

(to the **LISTSERV** address, of course).

### **OPTIONS**

You can set any of several optional parameters to customize the way you interact with the list. All of these options are set by sending a command of the form:

`SET SEMNET *option*`

For example, by default SEMNET subscribers receive SEMNET message one at a time, as they are submitted. You may prefer to receive all of the SEMNET messages in one daily digest. To set the digest option, send the command:

`SET SEMNET DIG`\
(To reverse this, send: `SET SEMNET NODIG`)

By default, the SEMNET software does not acknowledge the messages sent to it, and subscribers do not receive copies of their own messages. This may leave subscribers wondering whether their messages have "gotten through." To get SEMNET to acknowledge your messages, send the command:

`SET SEMNET ACK`\
(To reverse this, send: `SET SEMNET NOACK`)

To receive copies of your own messages, send the command:

`SET SEMNET REP`\
(To reverse this, send: `SET SEMNET NOREP`)

### **LEAVING SEMNET**

To terminate your SEMNET subscription, send the command:

`SIGNOFF SEMNET`

### **THE ARCHIVES**

All messages sent over SEMNET are collected into monthly archive or log files. If you delete a SEMNET message you had planned to keep, or if you want to review an extensive discussion, you may want to retrieve the appropriate archive file.

There are two ways to retrieve the monthly archive files. The easier way is to visit Carl Ferguson's [Web archive site](https://web.archive.org/web/20190804223334/http://bama.ua.edu/archives/semnet.html). Alternatively, you can perform these functions by sending commands to the listserv address. Using the second option, you may retrieve monthly archive logs by using its code name: `LOG*yymm*`, where *yy* and *mm* are two-digit codes indicating year and month, respectively. So, to retrieve the archive file for March 1996, for example, send the command:

`GET SEMNET LOG9603`

By the way, because there **are** permanent archive files, SEMNET messages can be independently verified in ways that personal communications in general cannot be. Thus, when citing the contents of a SEMNET message in published works, it is a good idea to include a reference to the monthly log file from which the cited message may be retrieved.

### **SEARCHING THE SEMNET ARCHIVES**

Carl Ferguson's [Web archive site](https://web.archive.org/web/20190804223334/http://bama.ua.edu/archives/semnet.html) includes a convenient and easy-to-use real-time search capability. Alternatively, the LISTSERV software includes a limited search capability, which involves an arcane syntax. The following examples may serve as templates for your own searches:

The first sample command file searches for messages containing both of the words *word1* and *word2*. The search will be limited to SEMNET postings dated from January 1, 1995 to the present. The software expects the `search` command to appear on one physical line. If your `search` command extends beyond one line, use the `- `marker as a continuation character. The `index` command generates an index to all qualifying postings. Each index listing reports item #, date, time, size, and subject of the posting. The `print all` command returns the complete text of every message containing *word1* and *word2*.

`search *word1* *word2* -\
from 01 jan 95 to today in semnet\
index\
print all`

Here is a simpler sample job which searches for postings containing the word *RMSEA*, regardless of date. The complete text of these posting will NOT be returned because the `print all` command was not included.

`Search RMSEA in SEMNET\
Index`

The third sample job generates an index listing of all postings containing the exact **phrase** "*not positive definite*". The quotation marks limit the search only to messages containing the three words in this particular order. Without quotation marks, the search would turn up any message that included all three words, whether the words appeared together, in this order, or were scattered throughout the message.

`Search *"not positive definite"* in SEMNET\
Index`

The fourth sample job generates an index listing of postings sent by James *Steiger* which contained the words *RMSEA* AND *parsimony*.

`Search *RMSEA parsimony* -\
where sender contains *steiger* -\
in SEMNET\
Index`

When searching for a particular author, you may have to use the sender's email account number, rather than their real name. We expect eventually to have a more convenient Web-based search interface, but for now, you will have to do it the hard way.

### **FOR MORE INFORMATION**

More information about the software that runs SEMNET is available on request from LISTSERV itself. To get more extensive information about LISTSERV commands and options, send the command:

`INFO REFCARD`

To get more information about LISTSERV's search capabilities, send the command:

`INFO DATABASE`

The information will be sent by return e-mail--although there may be some delay.

* * * * *

Back to the [SEMNET FAQ](https://web.archive.org/web/20190804223334/http://www.gsu.edu/~mkteer/semfaq.html).\
Back to Ed Rigdon's [home page](https://web.archive.org/web/20190804223334/http://www.gsu.edu/~mkteer/index.html).

