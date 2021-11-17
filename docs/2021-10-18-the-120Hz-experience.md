_This article was first posted on our Rows.com "tech" Slack channel on 2021-10-19._

Today apple is announcing their next-gen laptops and chips. 

We will see, as it's expected, new Apple silicon with many important improvements over what was gen1 (Apple m1). We will also see other improvements: I think mostly focused on screens (ProMotion/ 120Hz?) and cameras, with at least 1080p with better FOV, head tracking, better light handling with ML. Battery bumps can be there or not, depending on how much power vs. weight they want - these are Pro machines anyway. A big question is how powerful will gpus be, and if apple will continue the tradition of custom sw (Metal etc) or if they'll support some other "standards" (DirectX OpenGL etc).

I think it's important to reflect on these announcements and general industry trends seriously. The following is my perspective.

As more power is given to the Front-End, I predict that we will be seeing more responsibilities being handed to local algorithms. 

- FE seems to enable more fluid, richer experiences. Local is faster, at least in what concerns latency and the computing budget. It is also more reliable as there's no outages, even though it also poses significant challenges like data sync. Finally, on the FE you can do better animations and richer multimedia.
- Local also enables more power to the users. Local-first software opens up the possibility of offline modes, an is important to decouple convenient online benefits like cloud storage, synchronization and collaboration from the ownership and portability of your data. Local software makes users the owners of what they do.
- 3D, for VR and AR, is even more possible with extra computing power, though that's of limited interest to many B2B SaaS companies like our own, [Rows.com](rows.com). 
- In 2021, a Back-end can't provide "120Hz Services" in real-time, that is, data and transformations that operate at the speed of modern, beautiful UIs. Probably they won't be able to do it for a long long time, given distances, network latency and unpredictable loads. 
- Candidates for local algorithms are search, computation (especially Image and Video processing) and of course interface rendering. At Rows in particular we are very hopeful, as we know first-hand how rendering large tables with millions of cells and thousands of icons and images can demanding. 
- Already we see an early indication that the industry is looking for those solutions, for example in the continued growth of productivity apps and services that are local-first or offer significant offline modes.
- Obviously there's the question of where in the FE one should offer an app, native or browser (or hybrid). More powerful computers also bolsters the browsers case. In my experience, web-development offers more compatibility at the expense of a worse user experience. In the browser, you have to compete for tab space, persistence and memory are limited and owned by the browser, which includes basic stuff like keeping you logged-in, and then you still have to pick and choose from a number of frameworks (e.g. react) that are all incomplete and offer less power (read, fps) and consistency (UI elements) than the native counterparts. It’s ok for apps you use a few times per week, but if you’re spending many hours per day on them, the lesser experience usually shows. If your productivity app is especially demanding (as spreadsheets are), being web-only or web-most is hard to justify.
- I definitely recommend this terrific article that pushes for this view, [Local-first Software](https://www.inkandswitch.com/local-first.html), by the Ink & Switch collective. It covers much more ground, and is more technical than this opinion of mine. 


At the same time, the more FE evolves, the more innovation will come to the BE too. 

- Already on ARM architectures, novel Infrastructure providers such as Cloudflare are being joined by traditional ones (AWS, GCP) to offer computation that is closer to the FE (edge), more cost efficient (ARM), more powerful (ML), and scalable (lambdas). Cloud services offer literally any kind of pre-built component you could wish for - state, realtime comms, cms, queues, DBs, etc.. 
- Separating and using future-proof components is critical, because any tools we adopt tend to stick around for a while and eventually become that beautiful monster called "technical debt". Components that do persistence (DBs), sync for state managmeent, and collaboration seem like safe bets on critical components.
- Novel things will continue to permeate into cloud systems, notably blockchains, as robust ways to own stuff and form consensus in a distributed world.

Some might think i'm relying too much on Apple's innovation for this view. Quite the contrary. Apple rarely predicts the future. But more frequently than any other company, they are the creator of the conditions for that future. Mac GUIs, the mouse, ethernet, wifi, iPod, iTunes, iPhone, App Stores, iPads, Apple Watches are creations that apple developed or unleashed at scale, and most of which became the basis of today's hardware and software economy. As an example, our company Rows can be traced to the iPhone: iPhone => iPhone scale => Massive-scale Apps => AWS => SaaS => SaaS VCs => Rows. 

In conclusion, I take from the Apple silicon efforts that that frontends are evolving to enable 120Hz, spearheaded by native frameworks, and that it'll be impossible for apps to take advantage of this fully while keeping tightly coupled FE-BE architectures. The most demanding (and pleasant) productivity systems should be the first to migrate to richer local experiences with cloud systems for storage, sync and collaboration. It will make sense that a decent chunk will go the native route, to take advantage of platforms to offer multi-device, native-like experiences. 

Let’s go!
