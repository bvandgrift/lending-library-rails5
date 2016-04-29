# README: Lending Library API

## Abstract

This codebase implements a lending library API, listing titles, authors,
lendable copies of books, and allowing users to sign up, contribute books,
and update title and author information.

## Purpose

This codebase exemplifies the implementation of most components of an
API using Rails and Grape. It can be used as an educational tool, a
reference, or the basis for beginning a new project or building a Rails
template.

## Rationale

Note, we're speaking mainly about Rails 4.x here.

_WHY RAILS?_ In many applications, there is some crossover between
the web application and the api. The basic rails setup is comfortable
and easily extended. Configuration is well-understood. In short, Rails
provides a set of environmental features that will facilitate development,
even if (as in this case), we aren't using controllers at all, and are
simply mounting rack apps using `config/routes.rb`.

In addition, many of the most common features in an API (authn/z, search,
etc.) can be found in well-established rubygems we can include. As a base,
Rails will serve us well.

Finally, Rails has a templating system we may be able to employ to
create an API in a very short time, by including everything we need
without setup. It is our hope that this humble example will form the
blueprint for such a template.

_WHY GRAPE?_ Grape contains all of the most critical features for API
construction, without a lot of the fluff. The HTTP method and parameters
are front and center. It's simple. It's fast. It's most of the things
you want out of an API.

Rails' methodology is one of web applications; while it's not late to
the API party, it's routing and controller structure hasn't been streamlined
to the same degree.

## Features

Endpoints for the following:

* A catalog of titles and authors
* A list of books available for loan
* User authentication and authorization
* Authenticated users can borrow a book by creating a loan
* Members can contribute a book
* Curators can update title and author information

## Methods

The application will:

* use test-driven practices
* use commonly used tools and gems
* use secure practices
* have baked-in deployment considerations
* be self-documenting
* include rational for architectural decisions
* be continuously integrated and delivered

## Getting Started

### Required:

* Ruby 2.3.0
* Postgres (or other database if you don't mind updating the Gemfile and
  configs)

### Setup:

* `bundle install`
* `bin/rake db:create db:migrate db:seed`
* `bin/rspec`

### Running:

* `bin/rails server`

## HOWTO

The steps for constructing this app (which may be used to create a
template in the future) can be found in [doc/howto.md](doc/howto.md).

## Copyright and License

The Lending Library API and accompanying text is &copy; Ben Vandgrift. The use
and distribution terms are covered under the [MIT License](http://www.opensource.org/licenses/MIT).
