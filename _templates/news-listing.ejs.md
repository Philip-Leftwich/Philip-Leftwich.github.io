```{=html}
<div class="news-listing">
  <% for (const [index, item] of items.entries()) { %>
    <% const itemId = `ni-${(item.path || `news-item-${index}`).replace(/[^a-zA-Z0-9_-]/g, "-")}`; %>
    <article class="news-listing__item<% if (!item.image) { %> news-listing__item--no-image<% } %>" aria-labelledby="news-item-title-<%= itemId %>">
      <% if (item.image) { %>
      <a class="news-listing__image-link" href="<%- item.path %>" aria-hidden="true" tabindex="-1">
        <img src="<%- item.image %>" alt="" class="news-listing__image">
      </a>
      <% } %>
      <div class="news-listing__content">
        <% if (item.date) { %>
        <div class="news-listing__meta"><%= item.date %></div>
        <% } %>
        <h3 class="news-listing__title" id="news-item-title-<%= itemId %>">
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
