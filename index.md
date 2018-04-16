---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "swc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
title: "FAIR Data and Software (Carpentries-based Workshop)"
venue: "Technische Informationsbibliothek (TIB)"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Welfengarten 1B, 30167 Hannover, Germany"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "de"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "52.38151,9.72025"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use http://www.latlong.net/)
humandate: "9-13. July 2018"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00-17:00"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2018-07-09      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2018-07-13        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Katrin Leinweber", "Angelina Kraft", "FINDMORE"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["FIXME"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["carpentries@tib.eu"]    # boxed, comma-separated list
collaborative_notes: https://hackmd.io/Z4LC40umSGKs0ycv3PC2Ow    # https://github.com/swcarpentry/workshop-template/issues/418
---

### General Information

**This workshop aims to train junior scientists in implementing the FAIR principles for research data & software management & development.** We want to help you identify similarities and differences between these two scientific objects and apply respectively appropriate good practices in preparing, publishing and archiving your work.
We will focus on one topic / principle per day, introducing its reasoning, benefits, and (differing and/or shared) implications for **research data/software management/development** together with the learners. We'll follow-up the theory-leaning introductions in the mornings with discussions and
live-coding sessions, using (Software & Data) Carpentry materials to illustrate and practice a principle's implementation in the [STEM](https://en.wikipedia.org/wiki/Science,_technology,_engineering,_and_mathematics) disciplines ("[MINT-Fächer](https://de.wikipedia.org/wiki/MINT-F%C3%A4cher)").
Regardless of discipline, learners are encouraged to bring questions about their own data and source code, we can answer those during the week.

<p align="center">
<em>
  It is a new, experimental workshop format that contextualises the highly practical lesson material from the <a href="{{site.swc_site}}">Software</a> and <a href="{{site.dc_site}}">Data</a> <a href="https://carpentries.org/">Carpentries</a> with the <a href="https://blogs.tib.eu/wp/tib/2017/09/12/the-fair-data-principles-for-research-data/">FAIR principles</a>
</em>
</p>


### For whom?

Junior scientists who wish to excel at
implementing the FAIR principles for research data and scientific
software. **You need to have some previous knowledge of the tools
that will be presented at the workshop.**


### When & Where?

Please see [events.tib.eu/fair-data-software
](https://events.tib.eu/fair-data-software/)
for all the details, including public transport directions and
[accommodation suggestions](https://events.tib.eu/fair-data-software/accommodation/). You can also find us on [OpenStreetMap
](https://www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16)
and [add the event to your Google
Calendar](https://calendar.google.com/calendar/render?action=TEMPLATE&text=FAIR Data and Software&dates={{ page.startdate | replace: "-", "" }}/{{ page.enddate | replace: "-", "" | plus: 0}}&trp=false&sprop&sprop=name:&sf=true&output=xml&location={{ page.address }}&details=Carpentries-based workshop at the {{ page.venue }}").


### Costs

**Participation is free of charge**. However, participants need to organise and pay for travel and [accommodation](#when--where) themselves. This workshop is part of an ideas competition supported by the [Jülich Research Centre](http://www.fz-juelich.de/portal/EN/Home/), and part of a [grant by the German Federal Ministry of Education and Research (BMBF)](https://www.bildung-forschung.digital/de/ideenwettbewerb-zum-digitalen-wandel-in-der-wissenschaft-2007.html).


### Food

At the workshop, snacks and drinks (fruits, biscuits, tea, coffee, mineral water), as well as both a vegan and a non-vegan lunch on each of the five days will be provided (free of charge). Participants will need to obtain breakfasts and dinners outside of TIB. Many cuisine options from bakeries and to restaurants are located within walking distance.


### Requirements

**Participants must bring a laptop with a Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on.** They should have a few specific software packages installed (listed [below](#setup)). They are also required to abide by the Carpentries' [Code of Conduct]({{site}}/conduct.html).

**Please note: This workshop focuses on the application** of the FAIR Principles on scientific data and software. Because it covers a variety of examples, it does require a basic knowledge of the tools listed in [the schedule](#schedule). If you are interested in learning these basics, please consider applying for one of the (non-experimental) [Software](https://software-carpentry.org/workshops/) and [Data](http://www.datacarpentry.org/workshops-upcoming/) Carpentry workshops, or [work through](https://software-carpentry.org/lessons/) their [material](http://www.datacarpentry.org/lessons/) in a self-paced manner.


### Accessibility

We try to make this workshop as accessible to everybody as
possible. If we can help you in any way, please
[get in touch](#contact) and we will attempt to provide.
We will prepare the venue to be **wheelchair-accessible** upon request.


### Recordings

We will record some or all of the lectures during this workshop and publish
them on the [TIB AV-Portal](https://av.tib.eu/). Discussion
sessions will not be recorded.


### Contact

If you have any questions, please don't hesitate to email us: [{{page.email}}](mailto:{{page.email}}).


### Registration Requests: [events.tib.eu/fair-data-software](https://events.tib.eu/fair-data-software/registration-request/)

---

## Schedule

{% comment %} DO NOT EDIT SURVEY LINKS {% endcomment %}
<p><em>Surveys</em></p>
{% if page.carpentry == "swc" %}
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif page.carpentry == "dc" %}
  <p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif page.carpentry == "lc" %}
<p>Ask your instructor about pre- and post-workshop Survey details.</p>
{% endif %}


We will focus on one topic / principle per day, introducing its reasoning,
benefits, and (differing and/or shared) implications for *proper research
data/software management/development* together with the learners. We'll
follow-up the theory-leaning introductions in the mornings with discussions and
live-coding
sessions, using (Software & Data) Carpentry materials to illustrate and
practice a principle's implementation in the
[STEM](https://en.wikipedia.org/wiki/Science,_technology,_engineering,_and_mathematics)
disciplines ("[MINT-Fächer](https://de.wikipedia.org/wiki/MINT-F%C3%A4cher)").
Regardless of discipline, learners are encouraged to bring questions about
their own data and source code, we can answer those during the week.


{% include schedule.html %}


### Collaborative Notes

We will use this <a href="{{page.collaborative_notes}}">collaborative
document</a> for chatting, taking notes, and sharing URLs and bits of code.

---

#### Syllabus
