---
title: "Visiting Scholars"
layout: single
permalink: /team/visiting/
classes: wide
sidebar:
        nav: "team"
team:
   - res: Jorge J. Locane
   - res: Paulo Lemos Horta
   ! (https://nyuad.nyu.edu/en/academics/divisions/arts-and-humanities/faculty/paulo-lemos-horta/_jcr_content/bio-info/image.adaptive.m1510293394259/394.jpg)
Paulo Lemos Horta is a scholar of world literature, the works, and authors who exert an impact beyond their cultures of origin. He is currently interested in the cross-cultural collaborations that influenced The Thousand and One Nights, and the reception of the works of 16th Century Portuguese author Luis de Camões, who lived in the Middle East and South Asia. His latest book, Marvellous Thieves: Secret Authors of the Arabian Nights will be published by Harvard University Press in January 2017.
His position in Abu Dhabi, long a cultural crossroads, will provide him a unique opportunity to further his study of both. He joins NYU Abu Dhabi from Simon Fraser University in Vancouver, Canada, where he was an assistant professor. There, he was instrumental in developing the university’s world literature program from the ground up. He is co-editing a volume for the MLA series Approaches to Teaching World Literature and has presented the results of his research on the 1001 Nights and world literature at Harvard, Cornell, Princeton, SOAS, and the Universidad de Sevilla. At Simon Fraser University he was the recipient of a World Literature and Cultural Research Grant and a President’s Research Grant.
   - res: Maud Gonne   
---
<section class="entries-grid">
{%- assign team = page.team -%}

{%- for r in team -%}

   <div class="grid__item-adjust">
   {%- assign person = r.res -%}
   {%- assign person = site.data.team[person] -%}
    {%- if person.url contains "://" -%}
      {%- capture person_url -%}{{- person.url -}}{%- endcapture -%}
    {%- else -%}
      {%- capture person_url -%}{{- person.url | relative_url -}}{%- endcapture -%}
    {%- endif -%}

      <article class="archive__item">
       <a href="{{- person_url -}}">

       <img src="
              {%- if person.avatar contains "://" -%}
                {{- person.avatar -}}
              {%- else -%}
                {{- person.avatar | relative_url -}}
              {%- endif -%}"
            alt="{%- if person.name -%}{{- person.name -}}{%- endif -%}">

         <h2 class="archive__item-title">{{- person.name -}}</h2>
         </a>

        {%- if person.bio-short -%}
         <div class="archive__item-excerpt">
         {{- person.bio-short | markdownify -}}
         </div>
        {%- endif -%}

      </article>
   </div>
{%- endfor -%}
</section>
