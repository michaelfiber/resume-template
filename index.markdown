---
layout: home
person: John Q. Public
contact: |
    1234 Main St
    New York City, NY 10001
    555-123-4567
    <a href="mailto:example@example.com">example@example.com</a>
summary: This is the professional summary for the top of the resume.
employment:
    - company: Blockchain Bros, Inc
      position: Chief Blockchain Analyst
      duration: May 2022 to Present
      summary: Helped achieve synergy in the blockchain space using AI.
    - company: Indistinct Chatter, LLC
      position: Assistant Screamer
      duration: April 2014 to May 2022
      summary: Oh my god the pain!
volunteer:
    - company: Borders Without Doctors
      position: Volunteer
      duration: June 1999 to April 2014
      summary: Change the world today.
education:
    - institution: Clown College
      attended: September 1995 to June 1999
      level_attained: Bachelor of Science in Jokeology
      
---

<!-- header -->
{:.person}
# {{ page.person }}

{:.contact}
{{ page.contact }}

{:.heading}
### Professional Summary

{{ page.summary }}
{:.summary}

{:.heading}
### Work Experience


<!-- employment section -->
{% for job in page.employment %}

#### {{ job.position }}, {{ job.company }}

{{ job.duration }} 
{:.duration}

{{ job.summary }} 

{% endfor %}


<!-- volunteer section -->
{% if page.volunteer.size > 0 %}

{:.heading}
### Volunteer Experience

{% for job in page.volunteer %}

#### {{ job.position }}, {{ job.company }}

{{ job.duration }} 
{:.duration}

{{ job.summary }} 

{% endfor %}

{% endif %}


<!-- education section -->
{% if page.education.size > 0 %}

{:.heading}
### Education

{% for edu in page.education %}

#### {{ edu.level_attained }}, {{ edu.institution }}

{{ edu.attended }} 
{:.duration}

{% endfor %}

{% endif %}