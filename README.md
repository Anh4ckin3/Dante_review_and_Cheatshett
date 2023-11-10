
# Revue du ProLab Dante de Hackthebox

Hey, je viens de finir le ProLab Dante ducoup je fais une petit review en FR parce que bah... il n'y en as pas beaucoup. 


## Sommaire 

- Post Dante 

- Comment j'ai trouvé le lab 

- Le contenu (sans spoil)

- Ce que j'ai appris 







## Post Dante

Avant de commencer, j'ai obtenu la certification EJPT de l'INE. Vous pouvez aller voir ma [Review](https://github.com/leandreonizuka/eJPTv2_reviewFR) à ce sujet.

Par la suite, j'ai fait pas mal de Rootme avec un objectif de 2000 points, ainsi que du Hackthebox où j'ai pu compléter le Path [Intro to Dante](https://app.hackthebox.com/tracks/Intro-to-Dante), que je recommande car il reflète bien le niveau de certaines machines stand-alone. J'ai également fait d'autres boxes, notamment celles orientées Active Directory (AD).

Côté Tryhackme, j'ai suivi la prépa AD qui comporte 6 modules qui ne m'ont pas plus convaincu que ça, mais ce n'est pas que mon avis. Grâce à cette prépa, j'ai pu augmenter mon niveau en AD et arriver assez serein pour les machines AD du prolab.

J'ai également suivi une introduction au buffer overflow, mais cela ne m'a servi à rien. Je vous expliquerai pourquoi plus tard.

Dernier point et non des moindres, le PIVOTING. C'était un peu flou pour moi car je n'avais jamais pu pratiquer, seulement un peu pendant l'EJPT mais c'était avec Metasploit. J'ai essayé de réaliser le pro lab sans Metasploit. J'ai voulu faire le module Hackthebox sur le pivoting, mais j'ai préféré faire ma veille et j'ai découvert [sshuttle](https://github.com/sshuttle/sshuttle) et [ligolo-ng](https://github.com/nicocha30/ligolo-ng) qui m'ont servi à faire tout le pivoting pour Dante.

## Comment j'ai trouvé le lab

Personnellement, c'était une bonne première expérience en simulation de pentest réelle, même si souvent c'était un peu CTF-like.

Pour ma part, le lab était très stable, donc c'était vraiment agréable de ne pas se faire couper sa session RDP ou son agent ligolo, car pour le coup, c'était un peu ma crainte au début.

En termes de difficulté, j'ai dû me challenger, notamment sur la partie PIVOTING. Le reste était tout à fait faisable en étant bien concentré. Néanmoins, je ne pense pas que quelqu'un qui sort de l'EJPT puisse se frotter à Dante, il vous manquera des connaissances en web, pivoting et en Active Directory, surtout si comme moi vous vous interdisais metasploit. 

## Le contenu

Vu qu'il faut commencer par quelque chose, commençons par... LE PIVOTING (je suis fier de moi en fait). Dante va vraiment être une bonne introduction à ce sujet en vous poussant vraiment à pivoter pour atteindre vos objectifs.

En ce qui concerne les machines Linux, le niveau était vraiment au même niveau que les machines du track Dante. Les footholds sont assez simples, même si parfois assez coriaces. Les privesc n'étaient pas excessivement difficiles ; si vous faites des machines easy HTB (Linux), les privilèges élevés ne devraient pas poser de problèmes.

J'ai trouvé plus de défis sur les machines Windows, entre les footholds bien pensés, l'abus de fonctionnalités, le password spraying, et les privesc qui m'ont fait revoir et maîtriser les bases (enfin, je pense) de l'élévation de privilèges sous Windows. J'étais vraiment content des machines Windows.

Je reste un peu sur ma faim en ce qui concerne Active Directory, c'était assez maigre en contenu et plutôt basique, même si j'ai entendu dire que c'était niveau OSCP. Donc pas de panique niveau AD, ça devrait aller si vous avez fait le path de Tryhackme et quelques machines easy de HTB.

Et du coup, cas particulier, je crois, mais j'ai pu contourner le buffer overflow et élever mes privilèges d'une autre manière. Le truc, c'est que la privilège était très simple, donc je crois qu'un petit malin faisait des choses sur la machine. C'était tout bénéf pour moi car je suis clairement mauvais en tout ce qui est reverse / buffer overflow =).

## Ce que j'ai appris 

Sans surprise, j'ai appris à utiliser des hosts compromis comme pivot pour accéder à d'autres sous-réseaux.

Être patient, précis et attentionné pendant l'énumération des machines. Je pense que Dante a aussi développé ma mentalité tryharder, car comme il n'existe pas de writeup du pro, je devais me documenter et apprendre de nouvelles techniques. D'ailleurs, comme disait maître Yoda, "Fais-le ou ne le fais pas, mais il n'y a pas d'essai", donc je devais le faire.

Lors des moments où je restais bloqué plus de 24 heures, j'ai pu compter sur des membres de la communauté infosec pour m'aider, notamment [Frozenk](https://www.youtube.com/@FrozenKwa) et [LightRadio](https://twitter.com/LightRadi0). Le discord de HTB est aussi là pour aider avec un chat dédié à Dante.

J'ai quelques conseils que j'aurais aimé avoir avant de commencer Dante :

- Notez tout ce que vous trouvez, notamment faites-vous une liste de mots de passe/utilisateurs.

- [Exegol](https://exegol.readthedocs.io/en/latest/index.html) est un bel atout et apporte un côté professionnel à la complétion du prolab.

- N'oubliez faire tout le processusse de post-exploitation sur une machine compromise.(recolte des creds, etc...)
