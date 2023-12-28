---
layout: gridlay
title: Team
subtitle: Neurophysiology and Neuroengineering Lab Members
---

# **Team**

<div class="clear"></div>

<div class="container">
  <div class="jumbotron jumbotron-correct">
      <p>
        Understanding complex neural systems at the functional level often requires novel advanced tools which can only be created with a profound grasp of neurophysiology. A multidisciplinary effort is needed, and our research team brings together researchers from biological and engineering sciences to solve complex problems in systems neuroscience.
      </p>
  </div>
</div>

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
          <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"><span class="fa fa-graduation-cap" aria-hidden="true"></span> Google Scholar </a> <br>
        {% endif %}
        {% if person.orcid %}
          <a href= "https://orcid.org/{{person.orcid}}" target="_blank"><span class="fa fa-book" aria-hidden="true"></span> ORCID </a> <br>
        {% endif %}
        {% if person.twitter %}
          <a href= "http://twitter.com/{{person.twitter}}" target="_blank"><span class="fab fa-twitter" aria-hidden="true"></span> @{{person.twitter}} </a> <br>
        {% endif %}
        {% if person.website %}
          <a href= "{{person.website}}" target="_blank"><span class="fa fa-rss" aria-hidden="true"></span> {{person.website}} </a> <br>
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
          <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"><span class="fa fa-graduation-cap" aria-hidden="true"></span> Google Scholar </a> <br>
        {% endif %}
        {% if person.orcid %}
          <a href= "https://orcid.org/{{person.orcid}}" target="_blank"><span class="fa fa-book" aria-hidden="true"></span> ORCID </a> <br>
        {% endif %}
    </div>
    <div class="col-sm-8" style="text-align: justify">
        {{person.description | markdownify}}
    </div>
</div>
{% endfor %}

<hr>

# **Alumni**

<hr>
<table>
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

<hr>

# **Undergraduate Students**
<hr>
<table>
    
  <tr>
    <th>Name</th>
    <th>Degree/Program</th>
    <th>Year</th>
  </tr>

  {% for undergrads in site.data.Undergrads %}

  <tr>
    <td>{{undergrads.name}}</td>
    <td>{{undergrads.position}}</td>
    <td>{{undergrads.years}}</td>
  </tr>
  
  {% endfor %}
    
  </table>