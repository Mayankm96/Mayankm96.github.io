---
layout: page
title: projects
permalink: /projects/
description: A collection of my research activities.
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}

### other relevant projects

* Survey on Variational Autoencoders for Bayesian Inference ([report](/assets/documents/projects/cs698-report.pdf))
* Visual Odometry using careful Feature Selection and Tracking ([report](/assets/documents/projects/ee698-report.pdf), [code](https://github.com/Mayankm96/Stereo-Odometry-SOFT))
* MATLAB based GUI for Motion Planning ([code](https://github.com/Mayankm96/Motion-Planning-GUI))
* Failure Handling in Swarm of Quadrotors ([report](/assets/documents/projects/cs637-report.pdf))
