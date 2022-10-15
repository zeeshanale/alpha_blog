Alpha Blog - A ROR application




<% @articles.each do |article| %>
<div class="row justify-content-md-center">
    <div class="col-7 mt-4">
        <div class="container card text-center shadow mb-5 bg-body rounded" id="art-card">
        <div class="card-header fst-italic">
            by Zeeshan
        </div>
        <div class="card-body">
            <h5 class="card-title "><%= link_to article.title, article_path(article), class: "text-success text-decoration-none" %></h5>
            <p class="card-text"><%= truncate(article.description, length: 50) %></p>
            <%= link_to 'Show', article_path(article), class: "btn btn-outline-success" %>
            <%= link_to 'Edit', edit_article_path(article.id), class: "btn btn-outline-info" %>
            <%= link_to 'Delete', article_path(article), method: :delete, data: {confirm: "Are you sure?"}, class: "btn btn-outline-danger" %>
            <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        </div>
        <div class="card-footer text-muted">
            2 days ago
        </div>
        </div>
    </div>
</div>
<% end %>