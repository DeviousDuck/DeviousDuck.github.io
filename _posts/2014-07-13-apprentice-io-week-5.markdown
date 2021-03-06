---
layout: post
title:  "Apprentice.IO - Week 5"
date:   2014-07-13 20:14:55
categories: thoughtbot apprenticeship month-2
---

This last week I've spent time getting comfortable with my new mentor's client
project. The first few days were a little frustrating. The application in
question was originally a dot net application which was then converted to a
Rails 2 app. However, most of the developers originally on the project didn't
have a lot of experience with Ruby or Rails so the application has some oddities
that I presume come from Ruby not being their first language.

Something I'm quickly beginning to realise, which I didn't fully appreciate
before becoming a developer, is that your language really shapes the way you
think. There are concepts core to some languages which just don't fit into
others. As my only real experience is with Ruby and JavaScript I'm not really
comfortable commenting more on this observation, however, I hope I can keep my
mind open enough so that I don't end up writing Ruby code into whatever language
I decide to pick up next.

My mentor and I spent a day and a half refactoring a simple email notifier in a
rather large controller. I'm learning a ton about how to decouple strongly
coupled code. This exercise took longer than expected, and the results weren't
perfect, but it was a step in the right direction and we felt much better about
the code then when we started. We started by writing a bunch of controller specs
to make sure we didn't break anything then went ahead an refactored. The reason
for diving into this in the first place is we had a bug where 4 emails were
being sent to each recipient instead of 1. The mailer would need to send emails
to multiple recipients so we wrote specs to check these were getting sent.
Initially the specs were written without checking the body of the message. Once
these were all passing we added the additional expectation and received an odd
failure case. The thing that confused us the most is that we'd be checking the
"assignee" received the message and our expectation would return a non match but
show us a comparison with the message the "author" should be receiving. It turns
out the message we were checking we has mistyped. It seems that rspec when
comparing expectations will loop through all the possible matches and if it
doesn't find one will output a failure with the first non match compared to your
expected value. This makes sense but was slightly jarring when it came up.

The other apprentices and I have starting doing an apprentice stand up every
week where we talk about what we're doing. We decided it would be cool to make a
group breakable toy, and did a small design sprint for a online version of
diplomacy. We decided to write the application using ember with a Rails api.
There was also talk of doing a lightning talk about it at this years summer
summit giving us a deadline of 5 weeks to have mvp. This seems like a good thing
as it lights a fire to get things done. We're planning to open source the
project so I'll post here once we're ready to show it off.

I went to my second Boston Ruby meetup and my first Boston Ember meetup. Both
were utterly fantastic and if your in the Boston area and not going to these or
something similar then your missing out on a awesome free resource. Both
communities are active and full of energy. I can't express how privileged it is
to work in this environment. Being surrounded by others with such passion for
what they do is truly remarkable.
