Úvod
****

Ačkoli mluvíme o Linuxu, ve skutečnosti myslíme určitou distribuci Linuxu. Mezi desítkami či spíše
stovkami distribucí Linuxu je již mnoho posledních let oprávněně nejrozšířenější Ubuntu, které
vychází z distribuce Debian. Ačkoli informace uvedené v příručce lze použít i pro jiné distribuce,
než tyto dvě, konkrétní příklady a informace v této příručce jsme ověřovali v

* Ubuntu 16.04 LTS Server (Xenial) z dubna 2016
* Ubuntu 14.04 LTS Server (Trusty) z dubna 2014

Edice *Ubuntu Server* standardně neobsahuje grafické rozhraní, ale neliší se možnostmi od edice
*Ubuntu Desktop*. Instalátor Ubuntu Server je rovněž textový, ale také velmi podobný tomu
grafickému.

Většina informací v příručce předpokládá přítomnost pouze textového prostředí. Čas od času zmíníme 
i grafickou alternativu.

Vzhledem k blízké příbuznosti mezi Ubuntu a Debian je příručka téměř bez výjimky **platná i pro
distribuci Debian**. Těch několik rozdílů mezi těmito systémy vždy zdůrazníme. Kromě Ubuntu a 
Debianu informace platí samozřejmě i pro všechny deriváty těchto operačních systémů jako Kubuntu, 
Xubuntu, Lubuntu, Mint a další.

Bohužel vzhledem k někdy značným rozdílnostem mezi rodinami Ubuntu/Debian a ostatními distribucemi
jako RHEL (Red Hat Enterprise Linux), Fedora a SUSE (openSUSE, SUSE Linux Enterprise) nemusí být
informace vždy správné i pro tyto systémy.

.. important:: Většina kapitol je však natolik "univerzálně linuxová", že platí pro prakticky 
   jakoukoli současnou linuxovou distribuci. Snad jediná vyloženě specifická kapitola pro 
   Ubuntu/Debian je :ref:`instalace-sprava-programu`.

Historie Linuxu
===============

V této části si povíme některé sice netechnické, ale i tak důležité informace, které z vás udělají
lepšího správce. Není výjimečné, že správce Linuxu je současně i nadšeným fanouškem a propagátorem
těchto systému a proto by měl vědět některé podstatné údaje z historie Linuxu, Ubuntu a Debianu.

Linux vznikl v roce 1991 jako osobní projekt finského vysokoškoláka Linuse Torvaldse. Mělo se
jednat o svobodný operační systém unixového typu. Projekt vyvolal obrovský zájem a současný úspěch a
vliv Linuxu je asi nezpochybnitelný. Maskotem Linuxu je tučňák.

Ovšem Linux staví na mnohem starších kořenech, protože historie unixových OS sahá několik desítek
let zpátky. Za první unix se považuje projekt z roku 1969 vyvinutý AT&T Bell Labs. Značného
rozšíření dosáhl po roce 1976, kdy byl nabídnut zdarma univerzitám. Řada dnešních komerčních unixů
(HP-UX, Solaris, IRIX) vychází právě z AT&T Unixu.

Dalším významným unixem byl BSD Unix (Berkeley Software Distribution) z roku 1977, který má dodnes
několik populárních svobodných potomků (FreeBSD, OpenBSD, NetBSD). Maskotem BSD unixů je čertík.

Linux přímo nesdílí kód s AT&T ani BSD Unixem a svými vlastnostmi je někde uprostřed.

Distribuce Linuxu
=================

Úplně striktně vzato pod pojmem Linux myslíme "jen" samotné jádro operačního systému (*kernel*). To
sice zajišťuje klíčové funkce jako obsluha I/O (disky, soubory), síťový subsystém, ovladače ap., ale
samo o sobě netvoří funkční celek.

Jádro Linuxu může díky licenci GPL kdokoli použít a "přibalit" k němu další software, určit způsob
konfigurace, přizpůsobit použití pro určitý účel (desktop, server, multimédia, bezpečnost), atd.
Výsledku se pak říká linuxová distribuce.

V současné době existují desítky distribucí, dokonce možná stovky, pokud počítáme i jejich deriváty
(odvozené distribuce). Tato skutečnost je výhodou i nevýhodou. Linuxový svět je velkou velmi čilou
líhní technologických inovací, ale na druhou stranu si velká rozmanitost a svoboda vybírá svou daň v
podobě menší "uhlazenosti" a přehlednosti a někdy i stability kódu.

Ubuntu
------

Dlouhodobě nejrozšířenější distribucí je Ubuntu, na které se tento kurz především zaměřuje. Důvodem
masivního úspěchu je snadnost použití, perfektní podpora HW (většina HW funguje bez instalace
dodatečných ovladačů) a spolupráce s řadou výrobců (nejznámější partnerství je s Dell). 
S rozšířeností souvisí i komunita, která čítá tisíce nadšených dobrovolníků, kteří o Ubuntu píší a
diskutují, a tak je pravděpodobnost, že jste první s určitým problémem, téměř nulová.

.. rubric:: Verzování

První verze Ubuntu byla vydána v říjnu 2004 a nejmenovala se 1.0, ale 4.10, tedy ROK.MĚSÍC. Toto
verzovací schéma používá Ubuntu dodnes. Snadno tak víme, že např. Ubuntu 12.04 bylo vydáno v dubnu
2012.

Ubuntu je vydáváno v půlročních cyklech vždy v dubnu (verze X.04) a říjnu (X.10).

Jednou za dva roky je vydávána verze LTS (Long Term Support) s prodlouženou podporou na 5 let. LTS
verze jsou vhodné pro nasazení na servery a větší množství desktopů.

Běžná verze má podporu 9 měsíců a proto se méně hodí na server, ale pro desktop je určitě správnou
volbou. Zejména, chcete-li zkoušet novinky a mít vždy to nejnovější.

.. rubric:: Canonical a Mark Shuttleworth

Ubuntu z velké části vyvíjí společnosti Canonical, kterou založil v roce 2004 Mark Shuttleworth.
Mark byl známou osobní již dříve, a to díky založení společnosti Thawte (SSL ceritikáty), kterou
později výhodně prodal. Nejznámější je však Mark jako historicky druhý vesmírný turista, který se
podíval na Měsíc.

Slovo Ubuntu znamená v jazyce jihoafrického kmene Zulu "lidskost ostatním" nebo jen "lidskost".
Název vybral zakladatel Mark Shuttleworth, který je původem právě z Jihoafrické republiky.

.. rubric:: Deriváty

Samotné Ubuntu má řadu derivátů, které se liší svou specializací. Nejčastěji nahrazují jiné
grafické prostředí místo výchozího Gnome/Unity. Mezi nejznámějí patří např.

* Kubuntu -- Ubuntu s KDE grafickým prostředím
* Xubuntu -- Ubuntu s Xfce grafickým prostředním vhodné pro méně výkonné počítače
* Lubuntu -- Ubuntu s LXDE grafickým prostředním vhodné pro nejslabší počítače
* Edubuntu -- Ubuntu sestavené s programy pro školy

.. rubric:: Ubuntu Server

Každá verze Ubuntu je k dispozici také v "edici" Server. Ubuntu Server vychází z běžného Ubuntu
(někdy zvané Desktop).

Má k dispozici stejné APT repozitáře, ale odlišnost spočívá zvláště v nepřítomnosti grafického
prostředí a tím souvisejícího GUI software. Také se trochu jinak instaluje, avšak jádro používá
stejné jako desktopové edice.

Ubuntu Desktop lze použít i pro serverové nasazení, ale Server edice bude fungovat rychleji, je
štíhlejší a sami postupně přijdete na to, že grafické prostředí ke správě nepotřebujete.

.. rubric:: Další varianty Ubuntu

Popularita Ubuntu je obrovská, a tak najdete oficiální i komunitní varianty Ubuntu téměř pro
jakékoli zařízení.

* Ubuntu TV -- Ubuntu určené pro výrobce set-top-boxů a tzv. smart televizorů.
* Ubuntu Touch -- varianta Ubuntu pro mobilní telefony a tablety, která umí nahradit Android na
  vašem mobilu
* Chromebook, PlayStation, Xbox -- pro všechen tento HW najdete deriváty Ubuntu, kterými můžete
  nahradit původní operační systém.

Debian
------

Debian a Ubuntu mají mnoho společného. Ubuntu vzniklo právě jako odštěpek (fork) od Debianu. Debian
je však přísně nekomerční, vyvíjený výhradně komunitou GNU okolo Free Software Foundation a
nadšenci. Dokonce jako jediná distribuce se oficiálně pyšní přídomkem "GNU/Linux".

Také název Debian má svůj romantický původ. Původní zakladatel Ian Murdock, tehdy student americké
Purdue University, pojmenoval projekt podle kombinace jména své přítelkyně Debra a svého Ian.

Debian je znám svou konzervativností. Verze nejsou vydávány tak často jako Ubuntu a neobsahují vždy
nejnovější verze software, ale na druhou stranu je Debian považován za velmi spolehlivý a odladěný
systém.

Jako jediná masivně rozšířená distribuce za sebou nemá velkou firmu. Téměř celý systém je skutečně
vyvíjen komunitou nadšených a talentovaných lidí.

Ubuntu využívá systém balíčků a software původně navržený pro Debian, ale poslední dobou najdeme i
obrácený směr symbiózy - technologie z Ubuntu se dostávají do Debianu.

Red Hat a Fedora
----------------

Red Hat býval v 90. letech synonymem pro Linux. Nyní má společnost Red Hat placený produkt Red Hat
Enterprise Linux (RHEL) a volně přístupnou Fedoru s nejistou koncepcí, budoucností a menší
uživatelskou komunitou. Tímto rozdělením a především zpoplatněním dost ztratil na svém rozšíření.

Na druhou stranu se cílení RHEL na velké podniky finačně vyplácí. Red Hat je silná a prosperující
firma. Mimo velké podniky je jeho nasazení, vzhledem k vysokým licenčním poplatkům, málo časté.

SUSE a openSUSE
---------------

Distribuce SUSE má také dlouhou historii a těší se oblíbenosti rovněž ve velkých podnicích. Původně
malá německá firma stojící za SUSE byla koupena společností Novell, ale ta byla sama v roce 2011
prodána Attachmate Group a SUSE se nyní vyvíjí v rámci této firmy jako samostatná obchodní jednotka.

SUSE se před relativně dlouhou dobou rozhodla pro podobný krok jako Red Hat a rozdělila se na
placený SUSE Linux Enterprise (SLE) a volný openSUSE.

SUSE je pravděpodobně třetí a poslední rozšířenější verzí Linux, o které běžně uslyšíte. Často je
považována za "nejuhlazenější" Linux vůbec.

Která distribuce je ta nejlepší?
--------------------------------

Doufáme, že zde opravdu nečekáte odpověď :-) Ta totiž závisí na tom, jak chcete Linux používat, jaké
máte znalosti Linuxu a jaká další kritéria posuzujete (stabilita, rozšířenost, úroveň podpory).

Myslíme si však, že Ubuntu má pozici nejrozšířenější linuxové distribuce oprávněně. A to vzhledem k
poměru ceny (zadarmo), funkčnosti a snadnosti použití.

Líbí se nám, že na rozdíl od Red Hat a SUSE můžeme vytvořit jakoukoli infrastrukturu bez ohledu na
náš rozpočet. Oproti Debianu považujeme za výhodu větší komunitu, lepší podporu hardware a pro
kritické nasazení můžeme přikoupit `podporu od výrobce Ubuntu Advantage 
<https://www.ubuntu.com/support/plans-and-pricing>`_.

Knihy a weby
============

Na závěr úvodní části bychom vás chtěli upozornit na některé knihy a weby, které považujeme za
vhodný zdroj dalších informací.

* *kniha a web Linux: dokumentační projekt* -- `anglický web projektu <http://www.tldp.org>`_ nebo 
  `česká kniha <http://www.root.cz/knihy/linux-dokumentacni-projekt-4-vydani/>`_ z těchto návodů.
  Tato kniha byla dříve k zakoupení u nakladatelství `CPress <http://knihy.cpress.cz>`_, ale již
  není v nabídce.
* *kniha Linux kompletní příručka administrátora* od CPress.
* *magazín Root* - http://www.root.cz
* *magazín AbcLinuxu* - http://www.abclinuxu.cz
* *magazín Linuxsoft* - http://linuxsoft.cz
* *weby Ubuntu.cz* a zejm. *wiki.ubuntu.cz* -- http://www.ubuntu.cz, http://wiki.ubuntu.cz
