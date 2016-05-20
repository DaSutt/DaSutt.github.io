.. title: Into Darkness Postmortem
.. slug: into-darkness-postmortem
.. date: 2016-05-20 15:23:46 UTC+02:00
.. tags:
.. category:
.. link:
.. description:
.. type: text

=============
Introduction
=============

Into Darkness is a top down isometric shooter game I developed with four other
students in a practical course during one semester at TUM. We decided to write
the whole game from scratch using C++ and DirectX. This proved to be quite a different
experience than other projects I did before. I will add more information on the
project page in the next time. In this post I want to give an overview of my experiences
during this project.

============
The Positive
============

I really liked the setting of our game. Our vision was to create a game where the
player would explore abandoned underground places and try to gather needed resources.
The idea was to increase the danger in form of aliens attacking the player while going
deeper underground. In the same way the player would find more resources in lower levels.
We wanted that light would play an important role both as an atmospheric element
and as a game mechanic to be used against the underground dwelling aliens. Overall
I think that could have created a quite interesting game experience.

The best thing of the whole project was to develop the whole game from scratch.
While it was a lot of work it was also a great experience and a lot of fun to
see the game grow continually from nothing. For it was far more rewarding to get a
feature running properly than just using a pre made game engine like Unity.
Even though the progress is obviously a lot slower compared to using an engine you
can really understand what is running under the hood of the game.

==============
The Challenges
==============

Concept Phase
-------------

While the initial concept definitely was interesting we made the mistake to not
concentrate on one specific feature but had a really broad set of features we wanted
to create. This especially proved a problem later in the development because we
had to divide our time between them instead of focusing on one at a time.
The general design was too ambitious to be achieved in the time we had.

During the course we had to create a physical prototype before starting with the
development. While I can understand why one could use this to test an initial prototype
it is not usable during later development in my opinion. The game play can not
really transferred to the paper prototype. It would have been more useful to use an engine
to create small game play prototype during the development.

Programming
-----------

Because of our design we started from the start to create systems specially for this,
making assumptions how we could improve the implementations early on. This was a
mistake which became apparent later in development when the requirements changed.
We had to change systems completely which would not have been such a problem if
we had started with a more flexible, general approach.

Something we did not do during development was code review leading to quite interesting
commits from team members. Sometimes the game would not work almost at all
after changes made and we had to get back to previous commits.

One problem during the development was definitely the lack of experience. Especially
the interaction between the different game components was quite hard. I would have
preferred to have someone with industry experience to provide some guidance during the
project.

Art
---

A problem we had with most of our student game projects was the lack of artists.
If only programmers are on your team it will definitely show in the resulting assets.
For the project I did most of the modeling and texturing myself. Looking back at
the results which are more like placeholders than real art I think the realistic
art style was not the right decision. Some more abstract rendering would have helped
to make the game look more finished in my opinion.

Team management
---------------

Because most of the initial design was my idea and I also had done some of the basic
engine programming already I was really interested in getting stuff done for the game.
Due to this I tried to do as much as possible myself leading to a bad task
distribution overall.

Task distribution in general proved to be quite some problem. There was a
difference in experience between the different team members which made it harder
to get important features done on time and with the correct quality. Communication
is really important to find out if a given task can be solved by the assigned
team member. We also had a new team member joining us almost at the end of the project.
Without much documentation it was quite hard for him to join the development.

Another aspect of team management which did not always work was team motivation.
As with most other university projects some people see it more as an easy way
to get credits instead of working on the game. Fortunately, most of us were motivated
in the beginning. However, with the increasing complexity and more and more time constraints
in the end, this became a problem. To prevent this communication again is really
helpful. Not addressing problems like this right away can damage the relationship
between the team members really fast.

==========
Conclusion
==========

By only looking of the final game I would say the project was not really successful.
This has different reasons: First the presentation of the final game is not polished
enough. The graphic and art style still look more like placeholders and most of the
menu and HUD are also placeholders. Second, the actual gameplay is not really fun
and has no really motivation for the player.

However, the overall project was a great learning experience for me. The challenges
I had to face would not have been present like this if we had created the
game using an existing game engine. Some of the things I would do differently next time
are:

- focus the design on one game element and test it
- use an engine for prototyping
- check if your game is actually fun to play
- let others test your game
- don't focus to early on optimizations
- Instead implement more flexible, general systems
- more communication between team members
- improve task distribution and don't try to do everything yourself
