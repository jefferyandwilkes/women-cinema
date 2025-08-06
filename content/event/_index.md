

```html
{{ $page := .page }}
{{ $content := .content }}
{{ $dateFormat := site.Params.date_format | default "Jan 2, 2006" }}

<div class="row">
  <div class="col-12 col-lg-4 section-heading">
    <h1>{{ with $page.Title }}{{ . | markdownify }}{{ end }}</h1>
    {{ with $content }}{{ . }}{{ end }}
  </div>
  <div class="col-12 col-lg-8">
    {{ $events := where site.RegularPages "Type" "event" }}
    
    <!-- Get current date for comparing with event dates -->
    {{ $now := now }}
    
    <!-- UPCOMING EVENTS -->
    {{ $upcoming_events := where $events "Params.date" "ge" $now }}
    {{ $upcoming_events := sort $upcoming_events "Params.date" "asc" }}
    
    {{ if $upcoming_events }}
    <div class="mb-5">
      <h3>Upcoming Events</h3>
      {{ range $upcoming_events }}
        {{ partial "event_card.html" . }}
      {{ end }}
    </div>
    {{ end }}
    
    <!-- PAST EVENTS -->
    {{ $past_events := where $events "Params.date" "lt" $now }}
    {{ $past_events := sort $past_events "Params.date" "desc" }}
    
    {{ if $past_events }}
    <div>
      <h3>Past Events</h3>
      {{ range $past_events }}
        {{ partial "event_card.html" . }}
      {{ end }}
    </div>
    {{ end }}
  </div>
</div>
```
