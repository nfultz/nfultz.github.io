<!-- njnmdoc:  title="TGS Thoughts, part 2"  -->

Today (Feb 4, 2021) Google finally pulled TGS from the chrome store following
the ongoing discussion:

[Upcoming changes to the management of The Great Suspender #1175](https://github.com/greatsuspender/thegreatsuspender/issues/1175) and
[URGENT: SECURITY: New maintainer is probably malicious #1263](https://github.com/greatsuspender/thegreatsuspender/issues/1263)

This has been ongoing for eight months, but got popular on Twitter in January,
which lead to some mainstream coverage on HN, Lifehacker and The Register, among
others.

I used to use TGS heavily, because I usually have 100-300 tabs open at any one time.

# Easy fix for the impatient


A [clean fork](https://chrome.google.com/webstore/detail/the-marvellous-suspender/noogafoofpebimajpfpamcfhoaifemoa?hl=en)
has been posted on the chrome store by [gioxx](https://github.com/gioxx).

You can use that at your own risk.

# New Fork, Same Problems

However, switching to a fork does not address the root issue: that this kind of
code, although widely used, is not proportionally valued.

The original author closed over 800 issues over half a decade, mainly narrow
feature requests from internet randos with zero contributions themselves.
Although it was always possible to donate, so few people actually did that the
[donation link was dropped](https://github.com/greatsuspender/thegreatsuspender/pull/1135/commits/1608710a7164f8f3bb5783553f5542eb9941f3c3).

I never donated myself, but I at least tried to answer questions on GH and say thank you. I
had the same experience on other projects.

With that kind of constant, thankless, unpaid requests coming in, it's no surprise that the author
got tired and sold the software to someone else.

Even if you switch to a fork, there's no reason to expect that the same
thing won't happen again to the new person. Maybe it takes another seven years,
but the root cause is still there:

[Open Source Has A Funding Problem](https://stackoverflow.blog/2021/01/07/open-source-has-a-funding-problem/)

# API Rot is Coming

At the same time, Chrome will be upgrading its internal API to Manifest 3,
which will require changing the background pages with service workers.

This is work just to maintain the existing feature set, and will surely lead to
another wave of bug reports.

I hope the fork's author is mentally prepared for this - they should expect
zero support from Google nor "the community."

# Peer review is still needed

Although the new author is well intentioned, this and other recent extension
drama shows that the internal review system at Google is too slow to respond
and is letting bad code through. The fork needs the same amount of scrutiny
as the original if large numbers of people switch.

Google should acknowledge the fact that peer review flagged this several months
ago, dramatically increase the amount of transparency around extension
review, and accept peer reviews *before* millions of accounts are compromised.

# Crowdfunding an alternative

At some point in January, I thought "if only 1% of the 2 million users
contributed a dollar each, maybe this could be an actual professional product."

Instead of a side project that accidentally gets popular.

I'd already written some extensions before, but having only made $5.66 off
those, I wanted to validate the economics before I got myself stuck with another
800 issues on Github to deal with.

So I posted the idea on Kickstarter to see what would happen.  I set the goal
based on an estimate of total cost of long term support: 800 tickets * $40 =
$32000, and added 10% to cover Kickstarter fees.

As of today, here is my pledges funnel:

  * Direct
    * 202 Users
    * $2 Pledges
      * $1 is real
      * $1 is Kickstarter referral spam, which I had not imagined could be a thing.
  * Referral
    * 6 users from Github
    * $0 pledges
  * Organic Search
    * 6 users
    * $0 pledges
  * Paid Search
    * $52 spend
    * 1430 impressions
    * 59 users
    * $0 pledges
  * When I disclosed this project to my boss, he kicked in $10.

This is pretty underwhelming, imho, orders of magnitude less than the value of
the time and psychic energy this project could realistically require.

# Environmental impact grant

I also applied for an environmental micro grant for $1000,
based on the logic that suspending tabs extends device batter life and saves power.

I was told that the grant committee did not understand the impact. On the other hand,
in the past, they have been willing to award grants for catering when speakers visit,
and I don't really see the impact there, either.

C'est le vie.

# Alternative funding models

The other funding models are obvious, but also problematic:

  * Donations - did not work before.
  * Embedding advertising - Ick.
  * Pay-per-install - Google has removed payments from the web store, and my last extension made less than the developer fees cost.

One model I'm interested in is embedded licenses - these features could be
implemented as a drop-in library, and other, profitable companies could license
it from me and integrate the feature into, say, a start-page extension or
search extension. At the same time, I could offer a free, unbranded version for the
more technical users that are my peer group and might actually contribute back.

# Current status, future work

While I was waiting for the money to roll in, I wrote an MVP using Manifest 3
and posted it on Github. When Chrome 90 actually ships, maybe I'll upload it to the
Chrome Store just to see if there's interest.

In the meantime, I wish the TMS fork's maintainer luck and figures out a way to make it work.
