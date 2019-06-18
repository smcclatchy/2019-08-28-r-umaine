---
layout: workshop      # DON'T CHANGE THIS.
carpentry: ""
venue: "R for Reproducible Scientific Analysis"
address: "Barrows Hall Room 126, University of Maine, Orono, ME"
country: "us"
language: "en"
latlng: "44.9026398,-68.6672779"
humandate: "Aug 28-29, 2019"
humantime: "9:00 am - 4:30 pm"
startdate: 2019-08-28
enddate: 2019-08-29
instructor: ["Sue McClatchy", "TBD"]
helper: ["Michael Wilczek", "Angie Reed"]
email: ["susan.mcclatchy@jax.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite: 62589890046
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
frameborder="0"
width="100%"
height="280px"
scrolling="auto">
</iframe>
{% endif %}

<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
<strong>Where:</strong>
{{page.address}}.
Get directions with
<a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
or
<a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
<strong>When:</strong>
{{page.humandate}}.
{% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
<strong>Requirements:</strong> Participants must bring a laptop with a
Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.). They should have a few specific software packages installed (listed
<a href="#setup">below</a>). They are also required to abide by the
{% if page.carpentry == "swc" %}
Software Carpentry's
{% elsif page.carpentry == "dc" %}
Data Carpentry's
{% elsif page.carpentry == "lc" %}
Library Carpentry's
{% endif %}
<a href="{{site.swc_site}}/conduct.html">Code of Conduct</a>.
</p>

{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
<strong>Accessibility:</strong> We are committed to making this workshop
accessible to everybody.
The workshop organizers have checked that:
</p>
<ul>
<li>The room is wheelchair / scooter accessible.</li>
<li>Accessible restrooms are available.</li>
</ul>
<p>
Materials will be provided in advance of the workshop and
large-print handouts are available if needed by notifying the
organizers in advance.  If we can help making learning easier for
you (e.g. sign-language interpreters, lactation facilities) please
get in touch (using contact details below) and we will
attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
<strong>Contact</strong>:
Please email
{% if page.email %}
{% for email in page.email %}
{% if forloop.last and page.email.size > 1 %}
or
{% else %}
{% unless forloop.first %}
,
{% endunless %}
{% endif %}
<a href='mailto:{{email}}'>{{email}}</a>
{% endfor %}
{% else %}
to-be-announced
{% endif %}
for more information.
</p>

<hr/>

<hr/>

<h2 id="schedule">Schedule</h2>

<div class="row">
<div class="col-md-6">
<h3>Wednesday, Aug 28</h3>
<table class="table table-striped">
<tr> <td>09:00</td>  <td><a href="http://swcarpentry.github.io/r-novice-gapminder/">Workshop Overview</a></td> </tr>
<tr> <td>09:30</td>  <td><a href="https://r4ds.had.co.nz/workflow-basics.html">Workflow: basics</a></td> </tr>
<tr> <td>09:55</td>  <td><a href="https://r4ds.had.co.nz/workflow-scripts.html">Workflow: scripts</a></td> </tr>
<tr> <td>10:25</td>  <td><a href="https://r4ds.had.co.nz/workflow-projects.html">Workflow: projects</a></td> </tr>
<tr> <td>10:45</td>  <td>Coffee</td> </tr>
<tr> <td>11:00</td>  <td><a href="http://swcarpentry.github.io/r-novice-gapminder/03-seeking-help/">Seeking Help</a></td> </tr>
<tr> <td>11:20</td>  <td><a href="https://r4ds.had.co.nz/vectors.html">Vectors</a></td> </tr>
<tr> <td>12:30</td>  <td>Lunch break</td> </tr>
<tr> <td>13:30</td>  <td><a href="http://swcarpentry.github.io/r-novice-gapminder/09-vectorization/">Vectorization</a></td> </tr>
<tr> <td>13:45</td>  <td><a href="http://swcarpentry.github.io/r-novice-gapminder/07-control-flow/">Control Flow</a></td> </tr>
<tr> <td>14:45</td>  <td>Coffee</td> </tr>
<tr> <td>15:00</td>  <td><a href="http://swcarpentry.github.io/r-novice-gapminder/10-functions/">Functions Explained</a></td> </tr>
<tr> <td>16:25</td>  <td>Wrap-up</td> </tr>
<tr> <td>16:30</td>  <td>End</td> </tr>
</table>
</div>
<div class="col-md-6">
<h3>Thursday, Aug 29</h3>
<table class="table table-striped">
<tr> <td>09:00</td>  <td><a href="https://r4ds.had.co.nz/data-visualisation.html">Data Visualisation</a></td> </tr>
<tr> <td>10:45</td>  <td>Coffee</td> </tr>
<tr> <td>11:00</td>  <td><a href="https://r4ds.had.co.nz/transform.html">Data Transformation</a></td> </tr>
<tr> <td>12:00</td>  <td><a href="https://r4ds.had.co.nz/exploratory-data-analysis.html">Exploratory Data Analysis</a></td> </tr>
<tr> <td>12:30</td>  <td>Lunch break</td> </tr>
<tr> <td>13:30</td>  <td><a href="https://r4ds.had.co.nz/exploratory-data-analysis.html">Exploratory Data Analysis (continued)</a></td> </tr>
<tr> <td>14:00</td>  <td><a href="https://r4ds.had.co.nz/tibbles.html">Tibbles</a></td> </tr>
<tr> <td>14:30</td>  <td><a href="https://r4ds.had.co.nz/data-import.html">Data Import</a></td> </tr>
<tr> <td>14:45</td>  <td>Coffee</td> </tr>
<tr> <td>15:00</td>  <td><a href="https://r4ds.had.co.nz/tidy-data.html">Tidy Data</a></td> </tr>
<tr> <td>15:30</td>  <td><a href="https://r4ds.had.co.nz/r-markdown.html">R Markdown</a></td> </tr>
<tr> <td>16:00</td>  <td><a href="https://r4ds.had.co.nz/r-markdown-formats.html">R Markdown Formats</a></td> </tr>
<tr> <td>16:25</td>  <td>Wrap-up</td> </tr>
<tr> <td>16:30</td>  <td>End</td> </tr>
</table>
</div>
</div>

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.software-carpentry.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>
<table class="table table-striped">
<div class="col-md-6">
<h3 id="syllabus-r">Programming in R</h3>
<ul>
<li>Working with vectors and data frames</li>
<li>Reading and plotting data</li>
<li>Creating and using functions</li>
<li>Loops and conditionals</li>
<li><a href="https://www.rstudio.com/resources/cheatsheets/">Reference...</a></li>
</ul>
</div>
</table>
<hr/>
{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
To participate in a
{% if page.carpentry == "swc" %}
Software Carpentry
{% elsif page.carpentry == "dc" %}
Data Carpentry
{% elsif page.carpentry == "lc" %}
Library Carpentry
{% endif %}
workshop,
you will need access to the software described below.
In addition, you will need an up-to-date web browser.
</p>
<p>
We maintain a list of common issues that occur during installation as a reference for instructors
that may be useful on the
<a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>

<div id="r"> {% comment %} Start of 'R' section. {% endcomment %}
<h3>R</h3>

<p>
<a href="https://www.r-project.org">R</a> is a programming language
that is especially powerful for data exploration, visualization, and
statistical analysis. To interact with R, we use
<a href="https://www.rstudio.com/">RStudio</a>.
</p>

<div class="row">
<div class="col-md-4">
<h4 id="r-windows">Windows</h4>
<a href="https://www.youtube.com/watch?v=q0PjTAylwoU">Video Tutorial</a>
<p>
Install R by downloading and running
<a href="https://cran.r-project.org/bin/windows/base/release.htm">this .exe file</a>
from <a href="https://cran.r-project.org/index.html">CRAN</a>.
Also, please install the
<a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
Note that if you have separate user and admin accounts, you should run the
installers as administrator (right-click on .exe file and select "Run as
administrator" instead of double-clicking). Otherwise problems may occur later,
for example when installing R packages.
</p>
</div>
<div class="col-md-4">
<h4 id="r-macosx">macOS</h4>
<a href="https://www.youtube.com/watch?v=5-ly3kyxwEg">Video Tutorial</a>
<p>
Install R by downloading and running
<a href="https://cran.r-project.org/bin/macosx/R-latest.pkg">this .pkg file</a>
from <a href="https://cran.r-project.org/index.html">CRAN</a>.
Also, please install the
<a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
</p>
</div>
<div class="col-md-4">
<h4 id="r-linux">Linux</h4>
<p>
You can download the binary files for your distribution
from <a href="https://cran.r-project.org/index.html">CRAN</a>. Or
you can use your package manager (e.g. for Debian/Ubuntu
run <code>sudo apt-get install r-base</code> and for Fedora run
<code>sudo dnf install R</code>).  Also, please install the
<a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
</p>
</div>
</div>
</div> {% comment %} End of 'R' section. {% endcomment %}
