```{=html}
<div class="news-listing">
  <% for (const item of items) { %>
    <article class="news-listing__item">
      <% if (item.image) { %>
      <a class="news-listing__image-link" href="<%- item.path %>" aria-hidden="true" tabindex="-1">
        <img src="<%- item.image %>" alt="" class="news-listing__image">
      </a>
      <% } %>
      <div class="news-listing__content">
        <% if (item.date) { %>
        <div class="news-listing__meta"><%= item.date %></div>
        <% } %>
        <h3 class="news-listing__title">
          <a href="<%- item.path %>"><%= item.title %></a>
        </h3>
        <% if (item.description) { %>
        <p class="news-listing__description"><%= item.description %></p>
        <% } %>
      </div>
    </article>
  <% } %>
</div>
```
