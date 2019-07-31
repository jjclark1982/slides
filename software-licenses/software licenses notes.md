

Please join me for a seminar on common software licenses and the business models that love them.

We will discuss the risks faced by software projects and examine how a variety of organisations manages those risks through intellectual property licenses.

We will look at some public projects with a view to how you can build your open-source portfolio.




> “Every company is a software company”  
> — Satya Nadella, CEO of Microsoft (2017?)




> “The three chief virtues of a programmer are: Laziness, Impatience and Hubris.”  
> — [Programming Perl](http://wiki.c2.com/?LazinessImpatienceHubris), by Larry Wall (1991)






> “The continued adaptation, modification, and correction of errors in [programs] is essentially dependent on a certain kind of knowledge possessed by a group of programmers who are closely and continuously connected with them.”  
> — [Programming as Theory Building](http://pages.cs.wisc.edu/~remzi/Naur.pdf), by Peter Naur (1985)





# Software Licenses and Business Models


### Risks

What are the risks of being in the software business?

> “Many of the classic problems of developing software products derive from this essential complexity and its nonlinear increases with size. From the complexity comes the difficulty of communication among team members, which leads to **product flaws, cost overruns, schedule delays**. From the complexity comes the difficulty of enumerating, much less understanding, all the possible states of the program, and from that comes the **unreliability**. From complexity of function comes the difficulty of invoking function, which makes programs hard to use. From complexity of structure comes the **difficulty of extending programs** to new functions without creating side effects. From complexity of structure come the unvisualized states that constitute **security trapdoors**.”  
> — [No Silver Bullet](http://www.cs.nott.ac.uk/~pszcah/G51ISS/Documents/NoSilverBullet.html), by Fred Brooks (1986)

Software could kill someone

- [Therac-25](https://en.wikipedia.org/wiki/Therac-25) (1985–1987)
- [Sudden unintended acceleration](https://en.wikipedia.org/wiki/Sudden_unintended_acceleration) (1987–)
- [List of self-driving car fatalities](https://en.wikipedia.org/wiki/List_of_self-driving_car_fatalities) (2016–)
- [Boeing 737 MAX](https://www.wired.com/story/boeing-737-max-8-ethiopia-crash-faa-software-fix-lion-air/) (2018)

Software could destroy equipment or money or customers’ data

- [The Explosion of the Ariane 5](http://www-users.math.umn.edu/~arnold/disasters/ariane.html) (1996)
- [Knight Capital Says Trading Glitch Cost It $440 Million](https://dealbook.nytimes.com/2012/08/02/knight-capital-says-trading-mishap-cost-it-440-million/) (2012)
- [`Delete "$INSTDIR\boot.ini"`](https://www.eveonline.com/article/about-the-boot.ini-issue) (2007)
- [`rm -rf "$STEAMROOT/"*`](https://drj11.wordpress.com/2015/01/20/steaming/) (2015)

Software could allow an intruder to access our systems

- [Medtronic cardiac implant](https://en.wikipedia.org/wiki/Medtronic#Technology_safety) (2008–2011)
- [`goto fail`](https://nakedsecurity.sophos.com/2014/02/24/anatomy-of-a-goto-fail-apples-ssl-bug-explained-plus-an-unofficial-patch/) (2014)
- [Zoom video conferencing](https://www.schneier.com/blog/archives/2019/07/zoom_vulnerabil.html) (2019)
- Magic Lab robot intrusion incident (2012?)

Software could do something forbiddden by law

- [4-line RSA algorithm restricted by munitions export law](https://en.wikipedia.org/wiki/Export_of_cryptography_from_the_United_States) (1975–1997)
  - [Bernstein v. United States](https://cr.yp.to/export.html) (1996)
- [`09 F9 11 02 9D 74 E3 5B D8 41 56 C5 63 56 88 C0`](https://knowyourmeme.com/memes/09-f9-11-02-9d-74-e3-5b-d8-41-56-c5-63-56-88-c0) (2007)
- [Volkswagen emissions scandal](https://en.wikipedia.org/wiki/Volkswagen_emissions_scandal) (2008–2015)
- [List of GDPR Fines](https://alpin.io/blog/gdpr-fines-list/) (2018–)
- Patent infringement

Software could give incorrect analysis of strategic data

- [Nimbus-7 and Stratospheric Ozone](https://earthobservatory.nasa.gov/features/RemoteSensingAtmosphere/remote_sensing5.php) (1978–1985)

Software production could run over budget without producing usable results

- [List of failed and overbudget custom software projects](https://en.wikipedia.org/wiki/List_of_failed_and_overbudget_custom_software_projects) (1982–)

> “No amount of automation will have any significant effect on the size or efficiency of a bureaucracy.”   
> — [Why it is Important that Software Projects Fail](http://www.berglas.org/Articles/ImportantThatSoftwareFails/ImportantThatSoftwareFails.html), by Anthony Berglas (2008)

Unpleasant software could cause poor customer retention

- examples from the audience, please

### Liabilities

If we use software that causes damages, are we liable for those damages?

Did we get the software from some supplier?

Did the software include a warranty?

Does the law specify an [implied warranty](https://en.wikipedia.org/wiki/Implied_warranty) of merchantability or fitness for a particular purpose?

Does the implied warranty depend on the sale price?

> Australian businesses must guarantee products and services they sell, hire or lease for:
>
> - under $40,000
> - over $40,000 that are normally bought for personal or household use.
>
> — [Australian Competition and Consumer Act](https://www.accc.gov.au/consumers/consumer-rights-guarantees/consumer-guarantees) (2010)



If we publish software and it causes damages when someone else uses it, are we liable for those damages?



Why does software need a license? Why is copyright insufficient? Why are patents insufficient?

- Damage done by incompetent code (vehicular deaths)

- Damage done by malicious code (event-stream, ECDSA, compromised supply chain)

- Code that doesn't keep up with changing security requirements (ShellShock)

	- Insolvency or abandonment



### Types of Licenses

> “Each item of work being done on the project is to manage a particular risk.”  
> — [Risk-First Software Development](https://riskfirst.org/Quick-Summary), by Rob Moffat (2019)



Unlicensed software (in-house)

Outsourced software (for use in-house)

Proprietary software, licensed for customer use

- Example: Robot built-in OS, with binary blobs added to old kernel

Copyleft licenses (GPL)

- Example: Linux kernel

Industry-friendly open-source licenses (Apache) (includes patent grant)

- Counterexample: original React license

Unrestricted open-source licenses (MIT, BSD)

---

                            ---

                            Risk: People could discover vulnerabilities in the software.

                            Closed source

                            Unlicensed software (in-house)

                            Outsourced software (for use in-house)

                            Business Model: Snake Oil

                            ---

                            Risk: People could use the software in ways we do not want.

                            Proprietary software, licensed for customer use

                            Example: Robot built-in OS, with binary blobs added to old kernel

                            Example: Oracle Software License Auditing

                            Business Model: Hardware, Racketeering

                            ---

                            Risk: The software could become impossible to maintain. Or the software could enable other software that is impossible to maintain.

                            Copyleft licenses

                            - General Public License

                            Example: Linux kernel, bash, Git, MySQL, VLC, Audacity

                            Business Model: Consulting, Surveillance Capitalism

                            ---

                            Risk: The software could be unsuitable for anyone to use or contribute to. We could be liable for damage caused by the software.

                            Unrestricted open-source licenses

                            - MIT License

                            Example: Backbone.js - created by DocumentCloud to enable their product, used by others such as Trello

                            Example: Ruby on Rails - created by 37 Signals to enable their products, used by others

                            Example: GitLab, PuTTy, Node.js, Lua, Rust, Julia, Nim, Netlify CMS, NewsBlur (I pay for this)

                            Business Model: Contracting, Independent Software Vendor

                            ---

                            Risk: A user of the software could defame me.

                            Risk: The software could give incorrect results, with disastrous consequences at a nuclear facility.

                            - BSD License variants

                            Examples: CMake, CMU Sphinx, Dart, Go, Nginx

                            ---

                            Risk: Nobody could use the software without fear of lawsuit, because it is covered by some patent.

                            Industry-friendly open-source licenses

                            - Apache License (includes patent grant)

                            Example: Hadoop, Lucene, TensorFlow

                            Counterexample: original React license

                            Business Model: Enterprise Software



## References

https://paperswithcode.com/
https://ai.google/research/pubs/pub43146


http://yosinski.com/deepvis
http://www.evolvingai.org/synthesizing
https://thehive.ai/engineering/inside-a-neural-networks-mind
https://phillipi.github.io/pix2pix/
