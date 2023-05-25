---
layout: gridlay
title: Team
subtitle: Neurophysiology and Neuroengineering Lab Members
---

<div class="clear"></div>

# **Principal Investigators**
{% for person in site.data.PIs %}
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-3">
        <img class="img-responsive" src="{{person.image}}" {% if person.altimage %} onmouseover="this.src='{{person.altimage}}';" onmouseout="this.src='{{person.image}}';" {% endif %} alt="{{person.name}}"><br>
        <strong>{{person.name}}</strong> <br>
        {% if person.pronouns %}
           <em>{{person.pronouns}}</em> <br>
        {% endif %}
        {{person.position}} <br>
        {% if person.advisor %}
           {{person.advisor}}<br>
        {% endif %}
        <em>{{person.email}}</em> <br>
        {% if person.scholar %}
          <a href= "http://scholar.google.com/citations?user={{person.scholar}}"><span class="fa fa-graduation-cap" aria-hidden="true"></span> Google Scholar </a> <br>
        {% endif %}
        {% if person.orcid %}
          <a href= "https://orcid.org/{{person.orcid}}"><span class="fa fa-book" aria-hidden="true"></span> ORCID </a> <br>
        {% endif %}
        {% if person.twitter %}
          <a href= "http://twitter.com/{{person.twitter}}"><span class="fab fa-twitter" aria-hidden="true"></span> @{{person.twitter}} </a> <br>
        {% endif %}
        {% if person.website %}
          <a href= "{{person.website}}"><span class="fa fa-rss" aria-hidden="true"></span> {{person.website}} </a> <br>
        {% endif %}
    </div>
    <div class="col-sm-8" style="text-align: justify">
        {{person.description | markdownify}}
    </div>
</div>
{% endfor %}

<hr>

# **Members**
{% for person in site.data.LabMembers %}
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-3">
        <img class="img-responsive" src="{{person.image}}" {% if person.altimage %} onmouseover="this.src='{{person.altimage}}';" onmouseout="this.src='{{person.image}}';" {% endif %} alt="{{person.name}}"><br>
        <strong>{{person.name}}</strong> <br>
        {% if person.pronouns %}
           <em>{{person.pronouns}}</em> <br>
        {% endif %}
        {{person.position}} <br>
        {% if person.advisor %}
           {{person.advisor}}<br>
        {% endif %}
        <em>{{person.email}}</em> <br>
        {% if person.scholar %}
          <a href= "http://scholar.google.com/citations?user={{person.scholar}}"><span class="fa fa-graduation-cap" aria-hidden="true"></span> Google Scholar </a> <br>
        {% endif %}
        {% if person.orcid %}
          <a href= "https://orcid.org/{{person.orcid}}"><span class="fa fa-book" aria-hidden="true"></span> ORCID </a> <br>
        {% endif %}
    </div>
    <div class="col-sm-8" style="text-align: justify">
        {{person.description | markdownify}}
    </div>
</div>
{% endfor %}

<hr>

# **Undergrads & Alumni**
<hr>
<table>
    
  <tr>
    <th>Undergrad</th>
    <th>Years in Lab</th>
    <th>Degree</th>
  </tr>

  {% for alumni in site.data.Alumni %}

  <tr>
    <td>{{alumni.name}}</td>
    <td>{{alumni.years}}</td>
    <td>{{alumni.position}}</td>
  </tr>
      {% endfor %}
    
  <tr>
    <th>Alumni</th>
    <th>Years in Lab</th>
    <th>Position in Lab</th>
    <th>Subsequent Position</th>
  </tr>

  {% for alumni in site.data.Alumni %}

  <tr>
    <td>{{alumni.name}}</td>
    <td>{{alumni.years}}</td>
    <td>{{alumni.position}}</td>
    <td>{{alumni.nextPosition}}</td>
  </tr>

  {% endfor %}
</table>
