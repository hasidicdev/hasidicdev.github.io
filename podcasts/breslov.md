---
layout: page
title: Breslov Research Institute
---

#### "A Daily Dose of Rebbe Nachman"
* * *
<dl id="podcast-list"></dl>

<script>
$(document).ready(function() {
  $.get("https://v1.jewishpodcasts.fm/rss/548", function(data) {
    var items = [];
    $(data).find("item").slice(0,17).each(function(index) {
      var item = $(this);
      var title = item.find("title").text();
      var link = item.find("link").text();
      var date = item.find("pubDate").text();
      var calendarDate = new Date(date).toLocaleDateString();
      var description = item.find("description").text();
      var enclosure = item.find("enclosure").attr("url");
      var dt = 
      "<dt><a href='" + link + 
      "'>" + title + 
      "</a></dt><sup class='float-end'>" + calendarDate + 
      "</sup><dd>" + 
      "<audio src='" + enclosure + 
      "' controls></audio></dd>";
      $("#podcast-list").append(dt);
    });
  });
});
</script>