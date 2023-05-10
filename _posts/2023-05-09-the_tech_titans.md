---
layout: post
title:  "The Tech Titans"
categories: [ Team ]
image: assets/teams/the_tech_titans/the_tech_titans_intro-350px.png
comments: false
---


<div>
{% for team in site.data.teams.teams %}
    {% if team.teamname == "The Tech Titans" %}
    
    
    <h2> Team Members: </h2>
    <ul>
    
        {% for member in team.members.names %}
            <li><strong>{{ member }}</strong> - <em>{{ team.members.major[forloop.index] }}</em>  <br>{{ team.members.affiliation[forloop.index] }} <br>
            </li>
        {% endfor %}
             
       </ul>  
    <h2> Links: </h2>
     <ul>
    
        {% for link in team.links%}
        <li>
            {% if link.url contains '://' -%}
                <a href="{{ link.url }}"> {{ link.name }} </a> 
            {%- else -%}
                <a href="{{ link.url | relative_url }}"><i class="{{ link.icon }}" 
                style="color: {{ link.iconcolor }}"></i> {{ link.name }} </a> 
            {% endif %}
         </li>   
        {% endfor %}
             
       </ul>  
    {% endif %}
   
{% endfor %}
</div>

