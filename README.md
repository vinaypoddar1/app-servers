## Table of Contents
* [Scope](#scope)
* [Vagrant](#vagrant)
* [Languages](#languages)
  * [Ruby](#ruby)
  * [Elixir](#elixir)
  * [Node.js](#nodejs)
  * [GO](#go)
* [Benchmarks](#benchmarks)
  * [Hello World](#hello-world)

## Scope
The idea behind this repo is to have an environment where to test different application servers for disparate programming languages.  
The scope id to test out different langugages and at the same time verify the HTTP server implementation each langugage brings to the table.  
In the meantime i also tried to benchmark each server, althought i have to admit i had know how on Ruby only and i've applied no particular optimization to the others.

## Vagrant
As for the [ruby-app-servers](https://github.com/costajob/ruby-app-servers) repo i've used a vagrant box wth the following specs:
* Ubuntu Trusty 64 bit 
* 3 VCPUs (out of 4 of my MacBook Pro)
* 6GB of RAM

## Languages
I chose to make the tests on the following languages/runtimes: Ruby, Python, Elixir, GO, Node.js.
You'll notice i've not included any JVM language here: well, although i got two SUN certifications in 1996, my experience with the JVM had never made me happy.

### Ruby
[Ruby](https://www.ruby-lang.org/en/) 2.2 is installed by adding the
[brightbox](https://www.brightbox.com/docs/guides/cli/installation-debian/) repository.  
Ruby is the language i have more experience with.  
I find it an enjoyable language, although i start missing a serious support parallel processing, something quite "hot" on the uprising multi CPUs era.  

### Elixir
[Elixir](http://elixir-lang.org/) last version is installed by adding the
[erlang-solutions](https://www.erlang-solutions.com/about/erlang-other-technologies.html) repository.  
I studied Elixir last year, surfing the wave of Pragmatic Dave enthusiasm and finding its rubyesque resemblance pretty easy to grasp.  
Being based on Erlang it supports parallelism quite nicely and can leverage on some battle-tested frameworks.
What i dislike most is the complete lack of state: while i have invested too much time into OO techniques, i am not convinced pure immutability is required to get parallelism right.

### Node.js
[Node.js](https://nodejs.org/en/) stable version (4.x) is installed by adding nodesource repository.  
I once used to program in JavaScript much more that these days. I left it behind in
favor or more "backend" languages. I know it's a shame, since nowadays implementation of JS is quite fast, and the rise of Node.js has proven the language is much more than an in-browser tool.

### GO
[Go](https://golang.org/) language is installed by source.
Go is the favorite of mine between the "modern" languages: is simple, elegant and
fast. It compilies to native OS code and have CSP built in to favor parallelism.  
I am still exploring GO, but as far as i've gone i am pretty happy with it.

## Benchmarks
I decided to just test ow these languages manage multiple HTTP requests on some implementations. 
Talking about requests in Ruby is taboo, since the langugage (together with Python, Perl and PHP) has no native support for parallelism.
Some langugaes (GO and Erlang/Elixir) come with parallelism in mind, so i know is like comparing oranges and apples here.

### Hello World
The "application" i tested is barely minimal: is the HTTP version of the "Hello World" example.


