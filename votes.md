!SLIDE
# Allow voting on a topic

!SLIDE
# Votes
* Each vote will be an object (row in database table)
* When someone votes on a topic, we'll create a new vote object and save it
* Each vote is associated with a specific topic

!SLIDE
# Rails associations
* Topic has_many :votes
* Vote belongs_to :topics

!SLIDE
![has_many](http://www.gliffy.com/pubdoc/1735584/L.jpg)


