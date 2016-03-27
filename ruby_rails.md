## Ruby/Rails
* What are ruby gems?

+ Gems are package manager to download libraries into your app.

* What is the difference between a symbol and a string?

+ Symbols are immutable: Their value remains constant.

+ Multiple uses of the same symbol have the same object ID and are the same object compared to string
which will be a different object with unique object ID, every time.

+ You can't call any of the String methods like #upcase, #split on Symbols.

* What is the difference between a class method and an instance method?

+ Class methods are methods that are called on a class and instance methods are methods that are called on an instance of a class.

* What is the difference between local variables, instance variables, and class variables?

+ local variables: A local variable has a name starting with a lower case letter or an underscore character (_). Local variables do not, like globals and instance variables, have the value nil before initialization.

+ instance variables: An instance variable has a name beginning with @, and its scope is confined to whatever object self refers to. Two different objects, even if they belong to the same class, are allowed to have different values for their instance variables.

+ class variables: class Parent
  @@things = []
  def self.things
    @@things
  end
  def things
    @@things
  end
end


* What is a range?

+  Represents an interval—a set of values with a beginning and an end.
	(-1..-5).to_a      #=> []
	(-5..-1).to_a      #=> [-5, -4, -3, -2, -1]
	('a'..'e').to_a    #=> ["a", "b", "c", "d", "e"]
	('a'...'e').to_a   #=> ["a", "b", "c", "d"] 

* In ruby, what does attr_accessor do?  

+ Basically attr_accessor turn instance variable into instance method ( like @ no longer required ) in the class definition

* What is the purpose of environment files under the config folder in Rails? (development, test, production) (http://teotti.com/use-of-rails-environments/)

+ The purpose of those environments is to configure the Ruby on Rails framework

* What is the purpose of the application.rb file in Rails?

+ The purpose of this file is to configure things for the whole application like encoding.

* How can you define a constant?

?????????????? MyModule.const_set('MYCONSTANT','foobar')??????????????

* What is the purpose of `yield`?

+ As you use blocks, you will discover that the most common usage involves passing exactly one block to a method. This pattern is extremely popular in the Ruby world, and you'll find yourself using it all the time.

Ruby has a special keyword and syntax to make this pattern easier to use, and yes, faster! Meet the yield keyword, Ruby's implementation of the most common way of using blocks.

(https://rubymonk.com/learning/books/4-ruby-primer-ascent/chapters/18-blocks/lessons/54-yield)

* How do you store API keys when creating an app?

+ Easiest is to store the info as constants in your various environment files. That way you can use different accounts for development, production, etc.

+ # Eg
# development/environment.rb
....
API_1_USER = "user101"
API_1_PW = "secret!"

* How do I send parameters through a url?

+ Add them to the link <%= link_to "Add Product", '/pages/product?param1=value1&param2=value2' %>
+ Add them to the controller param1 = params[:param1] # "value1" param2 = params[:param2] # "value2"

* Explain MVC

+ Model, view, controller
+ (http://www.tomdalling.com/blog/software-design/model-view-controller-explained/)

* What is a `before_action`? When would you use it?

?????????????????

* What do controllers do in rails?

+ The Rails controller is the logical center of your application. It coordinates the interaction between the user, the views, and the model. The controller is also a home to a number of important ancillary services.

It is responsible for routing external requests to internal actions. It handles people-friendly URLs extremely well.

It manages caching, which can give applications orders-of-magnitude performance boosts.

It manages helper modules, which extend the capabilities of the view templates without bulking up their code.

It manages sessions, giving users the impression of an ongoing interaction with our applications.

* What is RESTful routing?

+ Action	HTTP Method
INDEX	GET
SHOW	GET
CREATE	POST
NEW	GET
EDIT	GET
UPDATE	PUT
DESTROY	DELETE

+ The aim of Restful Routing is to make you concious of your controllers.

* What is a polymorphic association?

+ Polymorphic association: a model can belong to more than one other model, on a single association

+ (https://launchschool.com/blog/understanding-polymorphic-associations-in-rails)

* What are params?

+ Params come from the user's browser when they request the page. For an HTTP GET request, which is the most common, the params are encoded in the url.

* How do I make a migration to add a column in Rails? (http://stackoverflow.com/questions/4834809/adding-a-column-to-an-existing-table-in-a-rails-migration)

+ If you have already run your original migration (before editing it), then you need to generate a new migration (rails generate migration add_email_to_users email:string will do the trick). Then do a rake db:migrate and it'll run the new migration.

If you have not yet run the original migration you can just edit it, like you're trying to do. Your migration code is almost perfect: you just need to remove the add_column line completely (that code is trying to add a column to a table, before the table has been created, and your table creation code has already been updated to include a t.string :email anyway).

* What is CSRF? How does Rails protect an app against this? (http://blog.bigbinary.com/2012/05/10/csrf-and-rails.html)

+ CSRF stands for Cross-site request forgery. It is a technique hackers use to hack into a web application.

+ In order to prevent such things from happening Rails uses authenticity_token.

* What's the difference between `User.find_by_id(1)` and `User.find(1)`?

+ (http://stackoverflow.com/questions/11161663/find-vs-find-by-vs-where)

* What's are classes in Ruby? What are modules? And what's the difference?

+ Modules: Modules are a way of grouping together methods, classes, and constants. Modules give you two major benefits:
	+ Modules provide a namespace and prevent name clashes.
	+ Modules implement the mixin facility.
