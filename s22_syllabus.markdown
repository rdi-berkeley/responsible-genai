---
layout: blank
title: "Decentralized Systems"
permalink: /s22_syllabus
---

<table style="table-layout: fixed; font-size: 88%;">
  <thead>
      <th style="width: 10%;">Date</th>
      <th style="width: 20%;"> Lecturer(s) </th>
      <th style="width: 50%;"> Topic </th>
      <th style="width: 20%;"> Module </th>
  </thead>
  <tbody>
    {% for row in site.data.syllabus %}
    <tr>
      <td> {{ row.date }} </td>
      <td> {{ row.lecturer }} </td>
      <td> {{ row.topic }} </td>
      <td> {{ row.module }} </td>
    </tr>
    {% endfor %}
  </tbody>
</table>

