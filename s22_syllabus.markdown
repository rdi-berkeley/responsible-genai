---
layout: blank
title: "Decentralized Systems"
permalink: /s22_syllabus
---

<table style="table-layout: fixed; font-size: 88%;">
  <thead>
      <th style="width: 10%;">Date</th>
      <th style="width: 10%;"> Lecturer(s) </th>
      <th style="width: 50%;"> Topic </th>
      <th style="width: 30%;"> Module </th>
  </thead>
  <tbody>
    {% for row in site.data.syllabus %}
    <tr>
      <td> {{ row.date }} </td>
      <td> 
        {% for l in row.lecturer %}
          {% if row.lecturer.link %}
            <a target="_parent" href="{{row.lecturer.link}}" style="text-decoration: underline;">{{row.lecturer.name}}</a>
          {% else %}
            {{ row.lecturer.name }}   
          {% endif %}
        {% endfor %}
      </td>
      <td> {{ row.topic }} 
        <br>
        {% if row.slides %}
        <ul style="margin-bottom: 0;">
          {% for s in row.slides %}
          <li> <a target="_parent" href="https://berkeley-defi.github.io/assets/material/{{s.file}}" style="font-size: 80%;"> Slides: {{ s.name }} </a> </li>
          {% endfor %}
        </ul>
        {% endif %}
      </td>
      <td> {{ row.module }}
        <br>
      </td>
<!--
      <td> 
        {% if row.reading %}
        <ul style="margin-bottom: 0;">
          {% for r in row.reading %}
            {% if r.file %}
              {% assign reading_link = 'https://berkeley-defi.github.io/assets/material/' | append: r.file %}
            {% endif %}
            {% if r.link %}
              {% assign reading_link = r.link %}
            {% endif %}
          <li> <a target="_parent" href="{{reading_link}}"> {{ r.name }} </a> </li>
          {% endfor %}
        </ul>
        {% endif %}
      </td>
-->
    </tr>
    {% endfor %}
  </tbody>
</table>

