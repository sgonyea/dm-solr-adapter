dm-solr-adapter
    by Lincoln Ritter and Matt Clark
    url http://github.com/winescout/dm-solr-adapter/tree/master

== DESCRIPTION:

DataMapper access to your Solr search repository

== FEATURES/PROBLEMS:

* Use solr to drive your models indipendent of any other datastore
* Batch inserts
* Inequality lookups(< >)

== SYNOPSIS:

  require 'dm-solr-adapter

  class Pencil
    include DataMapper::Resource
    property :brand, String, :key => true, :field => :brand_s
    property :composition, String, :key => true, :field => :composition_s
  end

  Pencil.new(:brand => "Berol", :composition => "graphite").save
  Pencil.all(:brand => "Berol")

== REQUIREMENTS:
dm-core
solr-ruby
addressable

== INSTALL:

git clone git://github.com/winescout/dm-solr-adapter.git
cd dm-dolr-adapter.git
sudo gem install

* You'll also want to cp /config/schema.xml into your Solr project
cp ./config/schema.xml <Apache-solr project root>/solr/config/

== LICENSE:

(The MIT License)

Copyright (c) 2008 FIXME (different license?)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
