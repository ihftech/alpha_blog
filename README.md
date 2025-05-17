# README

<div class="container">
  <% @articles.each do |article| %>
    <div class="row justify-content-md-center">
      <div class="col-8 mt-4">
        <div class="card text-center shadow mb-5 bg-white rounded">
          <div class="card-header font-italic">
            by Mashrur Hossain
          </div>
          <div class="card-body">
            <h5 class="card-title"><%= link_to article.title, article_path(article), class: "text-success" %></h5>
            <p class="card-text"><%= truncate(article.description, length: 100) %></p>
            <%= link_to "View", article_path(article), class: "btn btn-outline-success" %>
            <%= link_to "Edit", edit_article_path(article), class: "btn btn-outline-info" %>
            <%= link_to "Delete", article_path(article), class: "btn btn-outline-danger", method: :delete, data: {confirm: "Are you sure?"} %>
          </div>
          <div class="card-footer text-muted">
            <small>Created <%= time_ago_in_words(article.created_at) %> ago, 
            edited <%= time_ago_in_words(article.updated_at) %> ago</small>
          </div>
        </div>
      </div>
    </div>
  <% end %>
  </div>
</div>

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
