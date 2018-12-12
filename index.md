---
is_home: true
layout: default
---

<table class="f6 w-100 center pv2 pt4" id="posts-list" cellspacing="0">
  <thead>
    <tr>
      <th class="fw6 bb b--white tl pb2 pr3 w-10">Date</th>
      <th class="fw6 bb b--white tl pb2 pr3 w-25">Title</th>
      <th class="fw6 bb b--white tl pb2 pr3 w-55">About</th>
      <th class="fw6 bb b--white tl pb2 pr3 w-10"></th>
    </tr>
  </thead>
    <tbody class="lh-copy">
{% for post in site.posts %}	
<tr>
<td class="fw6 bb b--white tl pb2 pr3 w-10">{{ post.date | date: "%Y-%m" }}</td>
<td class="pv3 pr2 bb b--white w-25"><a href="{{post.url}}">{{post.title}}</a></td>
<td class="pv3 pr3 bb b--white">{{post.excerpt}}</td>
<td class="pv3 pr3 bb b--white">
<div class="flex flex-row-reverse justify-start h-100">
{% for tag in post.tags %}
<div class="tag tag-{{tag}}"></div>
{% endfor %}
</div>
</td>
</tr>
{% endfor %} 
</tbody>
</table>

