---
layout: blank
title: "Decentralized Systems"
permalink: /s22_syllabus
---

<table style="table-layout: fixed; font-size: 88%;">
  <thead>
      <th style="width: 20%;">Date</th>
      <th style="width: 80%;"> Topic </th>
  </thead>
  <tbody>
    {% for row in site.data.syllabus %}
    <tr>
      <th id="par" colspan="2" scope="colgroup"> {{ row.module }} </th>
    </tr>
      {% for lec in row.lectures %}
        <tr> 
          <td> {{ lec.date }} </td>
          <td> {{ lec.topic.title }}
            <br>
            {% if lec.topic.speaker %}
              Speaker: {{ lec.topic.speaker }} 
            {% endif %}
          </td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>

