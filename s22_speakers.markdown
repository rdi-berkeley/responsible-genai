---
layout: blank
title: "Decentralized Systems"
permalink: /s22_speakers
---

<table style="table-layout: fixed; font-size: 88%;">
  <thead>
      <th style="width: 20%;">  </th>
      <th style="width: 10%;"> Speaker </th>
      <th style="width: 70%;"> Brief Bio </th>
  </thead>
  <tbody>
    {% for row in site.data.speakers %}
      <tr>
        {% if row.picture %}
          <td><img style="object-fit:cover" width=150 height=200 src="/assets/{{ row.picture }}" alt={{ row.name }}></td>
        {% else %} 
          <td> </td>      
        {% endif %}
        <td> {{ row.name }} </td>
        <td> {{ row.bio }} </td>
      </tr>
    {% endfor %}
  </tbody>
</table>

