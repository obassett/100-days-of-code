# 100 Days Of Code - Log

### Day 1:July 13, 2018 
##### 

**Today's Progress**: Set up git repos for project and this one. did basic code to pull down tweets from twitter API. Will try to filter twitter api data tomorrow and be able to break it down.

**Thoughts:**: Long way to go, but at least first day is done.

**Link to work:** [Twitter Analysis (https://github.com/obassett/twitter-analysis)]

### Day 2:July 14, 2018 
##### 

**Today's Progress**: Spent the time working through process json data and understanding how to reference items in the data by using dictionary entries. Not a lot of actual saved code. Lots of reading and playing today to understand how it works. Set up basic kinesis stream to feed data into.

**Thoughts:**: being able to predictably access data out of what comes back from twitter api makes things easy. dictionaries are good for looking up data. Pushing tweets into a kinesis steam is particularly easy... consuming it may not be quite so easy

**Link to work:** [Twitter Analysis (https://github.com/obassett/twitter-analysis)]

### Day 3:July 15, 2018 
##### 

**Today's Progress**: Played Around with kenesis stream consumer that then fed the text of the tweets through AWS comprehend to do sentiment analysis. Super easy to use... really cool. Also learned what keyword arguments only means. Handy to know.

**Thoughts:**: Life sometimes makes it challenging to set aside time. Heopfully that will get easier as the habit forms... having an 8 month old however means late evenings are typically it for me. Need to work on making sure I am ready to go.

**Link to work:** [Twitter Analysis (https://github.com/obassett/twitter-analysis)]

### Day 4:July 16, 2018 
##### 

**Today's Progress**:  Wrote python to create Kinesis Stream so that I can create it at the beginning of hte day to cut my AWS costs while I am playing - Put it basic checking to make sure a stream with that name doesn't already exist. Also created deletion script.

**Thoughts:**:  It was interesting to read that [-1:] would return the last value of a list, and that if it was an empty list it would return an empty value rather than an exception. However meant that it was returning a list object rather than the string element. This took me a while to figure out that it was the : causing that. 

**Link to work:** [Twitter Analysis (https://github.com/obassett/twitter-analysis)]

### Day 5:July 17, 2018 
##### 

**Today's Progress**:  Started working freeCodeCamp since I need to learn some front-end stuff. Did the Basic HTML and HTML5 activities and then started on the Basic CSS and did the first few activities

**Thoughts:**:  CSS was brand new when I last touched HTML... it has been a while.

**Link to work:** N/A today since it was all on freecodecamp

### Day 6: July 18, 2018 
##### 

**Today's Progress**:  Worked Through freecodecamp CSS and then started on applied visual design.

**Thoughts:**:  So much to learn, and HTML has come a long way since HTML3

**Link to work:** N/A today since it was all on freecodecamp

### Day 7: July 19, 2018 
##### 

**Today's Progress**:  Slow night tonight, as I went out earlier. Finished the applied visual design section on freecodecamp

**Thoughts:**:  Wow, animation capabilities in basic HTML/CSS... kinda crazy.

**Link to work:** N/A today since it was all on freecodecamp

### Day 8: July 20, 2018 
##### 

**Today's Progress**:  Tired still, busy with work Managed to do the hour but slow going working through Applied Accessibility on FreeCodeCamp

**Thoughts:**:  lots to think about making sure the accessibility on a website is taken care of. 

**Link to work:** N/A today since it was all on freecodecamp

### Day 9: July 21, 2018 
##### 

**Today's Progress**:  Finished off the FreeCodeCamp Applied Accessibility and also Responsive Web Design Pricinciples

**Thoughts:**:  I like the idea of good accessibillity, and the concepts and ability to automatically adjust based on the size of the display being used to access content.

**Link to work:** N/A today since it was all on freecodecamp

### Day 10: July 22, 2018 
##### 

**Today's Progress**:  Finished All the lessons under Responsive Web Design. Now I need to start on the projects on FreeCofeCamp. Frst up will be the Tribute Page.

**Thoughts:**:  So far content has been relatively easy, I expect it will get a lot harded. Looking forward to the projects.

**Link to work:** N/A today since it was all on freecodecamp

### Day 11: July 23, 2018 
##### 

**Today's Progress**:  Today was about building out my tribute page for the FCC project. Trying to come up with one I wanted to do.

**Thoughts:**:   ...

**Link to work:** 

### Day 12: July 24, 2018 
##### 

**Today's Progress**:  Conintued working on my FCC Tribute page. It now works generally (and passes the test requirements). Content isn't finialised yet, and still toying with color schemes. 

**Thoughts:**:   

**Link to work:** 

### Day 13: July 27, 2018 
##### 

**Today's Progress**:  Started working through exception handling in Python. Learned all about try and except. Actaully useful and relatively straighforward (once you start actaully reading the docs for API's you are calling). Added error handling to the twitter stream, started looking at handling kinesis when you fill the shard, and how to split the add more shards. still wokring that out. Also think of siwthc from kinesis streams to firehose into S3 and using SNS on the back of that to handle the actaul sentiment analysis as I keep the history of the streams to go back to later, and also it might be easier to scale.

**Thoughts:**: Missing 2 days in a row sucked. But family comes first. Nice to get back to my own project for a bit rather than the tutorial project thing in FCC, but I need to get back to the rest of them soon.

**Link to work:** 

### Day 14: July 28, 2018 
##### 

**Today's Progress**:  Added a lot more exception handling to twitter pull script. Modified it to batch up the tweets before pushing into kinesis stream to improve performance and tested. Built in some degree of autoscale capability based on exceptions being thrown, but haven't been able to test yet as I can't seem to get it to throw the exception.

**Thoughts:**: Exception Handling ended up being a little harder than I though... forgot you needed to actually import the handlers from the libaries.

**Link to work:** 

### Day 15: July 29, 2018 
##### 

**Today's Progress**:  So found out that kinesis client doesn't throw the exception as an exception anymore but instead returns the error in the results and also returns a count. So wrote a bunch of code to process the error, detect the provisioned throughput exceeded error, capture the tweets to try again with and then pull the shard that I am going to split to increase performance. but then I read that you actually just want to increase the shard coutn (by double), rather than just splitting a single stream, to limit the operations... so I really didn't need to pull the shard name.

**Thoughts:**: RegEx's.... 

**Link to work:** 

### Day 16: July 30, 2018 
##### 

**Today's Progress**:  It all auotscales nicely etc... but I look at my code and what I need is to break it down into modules and functions. Ease the repitiion etc.

**Thoughts:**: should have started with a better plan and built modules and functions as I went. Ah well.

**Link to work:** 