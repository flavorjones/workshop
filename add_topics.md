!SLIDE
#let's add topics
* what exactly do we mean by "add topics?" 
* rails "scaffolding" to generate some pages (and code)
* set up database with a new table (migration)
* review what we did

!SLIDE
# adding topics
* topic will have a title and a description
* we will enable basic "CRUD" actions
  * Create - enter a new topic
  * Read - see everyone's topics
  * Update - change the topics you entered
  * Delete - remove your topics from the system 

!SLIDE
.

    ruby script/generate scaffold topic title:string description:text
    rake db:migrate

!SLIDE
.

    http://localhost:3000/topics

!SLIDE 
#What did we just do?
* a model
  * create    app/models/topic.rb
  * create    db/migrate/20090611073227_create_topics.rb
* 4 views
  * create  app/views/topics/index.html.erb
  * create  app/views/topics/show.html.erb
  * create  app/views/topics/new.html.erb
  * create  app/views/topics/edit.html.erb
* a controller
  * create  app/controllers/topics_controller.rb
  * route  map.resources :topics

!SLIDE
![Architecture](http://www.gliffy.com/pubdoc/1734447/L.jpg)

!SLIDE
# Model-View-Controller
* **Model**
  * represents what is in the database 
  * ActiveRecord
* **View**
  * the model rendered as HTML 
  * ActionView, erb
* **Controller**
  * receives HTTP actions (GET, POST, PUT, DELETE)
  * decides what to do, typically rendering a view 
  * ActionController

!SLIDE code
.

    git push heroku master
    heroku rake db:migrate
    git push
