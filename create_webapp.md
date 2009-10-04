!SLIDE
### Build and deploy a web application
* Add topics
* Vote on a topic
* Register and login

!SLIDE
<img src="http://www.ultrasaurus.com/rubyworkshop/app_design/authenticated_home.jpg" width="934" height="436"/>

!SLIDE
# Let's build a web app

!SLIDE

<code>
    rails suggestorama 
      -m http://gist.github.com/194076.txt 
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

!SLIDE code
&nbsp;  
    git init
    git add .
    git commit -m 'basic web application'

!SLIDE code
&nbsp;
    heroku create
    git push heroku master
