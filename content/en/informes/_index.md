---
title: "Informes"
linkTitle: "Informes"
menu:
  main:
    weight: 20
---

{{% blocks/section %}}

<div class="row row-cols-1 row-cols-md-2 row-cols-lg-2 g-4">
  {{ range (.Paginator 4).Pages }}
  <div class="col">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ .RelPermalink }}">{{ .Title }}</a></h5>
        <h6 class="card-subtitle mb-2 text-muted">{{ .Date.Format "2006-01-02" }}</h6>
        <p class="card-text">{{ .Params.description }}</p>
        <a href="{{ .RelPermalink }}" class="card-link">Ver más</a>
      </div>
    </div>
  </div>
  {{ end }}
</div>

<div class="mt-4">
  {{ template "_internal/pagination.html" . }}
</div>

{{% /blocks/section %}}
