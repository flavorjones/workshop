!SLIDE
# Build and deploy a web application
* Add topics
* Vote on a topic
* Register and login

!SLIDE
<img src="http://www.ultrasaurus.com/rubyworkshop/app_design/authenticated_home.jpg" width="934" height="436"/>

!SLIDE
# Tools we'll be working with
* **rails**
* **rake**: like make for ruby, easy way to run tasks
* **git**: for source code control
* **database**: we'll use sqlite, but could be any relational database 
* **editor**
* hosting services
  * **github**: source code repository 
  * **heroku**: free rails hosting

!SLIDE
# let's build a web app

!SLIDE

<code>
     rails suggestorama 
</code>

!SLIDE
<table>
	<tr>
		<th>File/Folder</th>
		<th>Purpose</th>
	</tr>
	<tr>
		<td><span class="caps">README</span></td>
		<td>This is a brief instruction manual for your application.</td>

	</tr>
	<tr>
		<td>Rakefile</td>
		<td>This file contains batch jobs that can be run from the terminal.</td>
	</tr>
	<tr>
		<td>app/</td>

		<td>Contains the controllers, models, and views for your application. You will mostly work here.</td>
	</tr>
	<tr>
		<td>config/</td>
		<td>Configure your application&#8217;s runtime rules, routes, database, and more.</td>
	</tr>

	<tr>
		<td>db/</td>
		<td>Shows your current database schema, as well as the database migrations. </td>
	</tr>
	<tr>
		<td>doc/</td>
		<td>In-depth documentation for your application.</td>

	</tr>
	<tr>
		<td>lib/</td>
		<td>Extended modules for your application (not covered today).</td>
	</tr>
	<tr>
		<td>log/</td>

		<td>Application log files.</td>
	</tr>
	<tr>
		<td>public/</td>
		<td>The only folder seen to the world as-is.  This is where your images, javascript, stylesheets (<span class="caps">CSS</span>), and other static files go.</td>
	</tr>

	<tr>
		<td>script/</td>
		<td>Scripts provided by Rails to do recurring tasks.  We'll use some today.</td>
	</tr>
	<tr>
		<td>test/</td>
		<td>Unit tests, fixtures, and other test apparatus.</td>

	</tr>
	<tr>
		<td>tmp/</td>
		<td>Temporary files</td>
	</tr>
	<tr>
		<td>vendor/</td>

		<td>A place for third-party code. </td>
	</tr>
</table>

!SLIDE
# run the web app 
!SLIDE code

    ruby script/server

    http://localhost:3000

!SLIDE
# make it your own
* modify public/index.html
* run it again

!SLIDE
# Awesome! Let's ship it!
* we'll create a local git repository
* then deploy to heroku

!SLIDE
<code>
    git init
    git add .
    git commit -m 'basic web application'
</code>

!SLIDE
<code>
    heroku create
    git push heroku master
    heroku rake db:migrate
</code>

!SLIDE
#push code to github
* create a repository
* follow the instructions

!SLIDE
<code>
    git config --global user.name "Your Name"
    git config --global user.email you@whatever.com
    git remote add origin git@github.com:yourgithubname/project.git
    git push origin master
</code>

!SLIDE
#switch computers

!SLIDE
<code>
    git clone git://github.com/yourgitname/project.git 
    git pull
</code>

!SLIDE
#let's add topics

!SLIDE
#CRUD
* Create - enter a new topic
* Read - see everyone's topics
* Update - change the topics you entered
* Delete - remove your topics from the system 

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

!SLIDE
# REST 
* Representational State Transfer
* Application state and functionality are abstracted into resources
* Each resource may be referenced with a global identifier (URI over HTTP)
* Resources share a uniform interfaces
* Note
  * introduced in 2000 in the doctoral dissertation of Roy Fielding
  * http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm

!SLIDE
# REST URIs and HTTP actions
* GET http://myserver.com/topics - a list of all the topics
* GET http://myserver.com/topics/1 - the first topic
* POST http://myserver.com/topics - create a topic
* PUT http://myserver.com/topics/1 - modify the first topic
* DELETE http://myserver.com/topics/1 - delete the first topic

!SLIDE
![Architecture](http://img.skitch.com/20090606-ebjqmem1ynptm4ta6qy72hg9ap.jpg)


