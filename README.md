# fib
FiB – Lets stop living a lie

### Inspiration
In the current media landscape, control over distribution has become almost as important as the actual creation of content, and that has given Facebook a huge amount of power. The impact that Facebook newsfeed has in the formation of opinions in the real world is so huge that it potentially affected the 2016 election decisions, however these newsfeed were not completely accurate. Our solution? FiB because With 1.5 Billion Users, Every Single Tweak in an Algorithm Can Make a Change, and we dont stop at just one.

### What it does
Our algorithm is two fold, as follows:

**Content-consumption:** Our chrome-extension goes through your facebook feed in real time as you browse it and verifies the authenticity of posts. These posts can be status updates, images or links. Our backend AI checks the facts within these posts and verifies them using image recognition, keyword extraction, and source verification and a twitter search to verify if a screenshot of a twitter update posted is authentic. The posts then are visually tagged on the top right corner in accordance with their trust score. If a post is found to be false, the AI tries to find the truth and shows it to you.

**Content-creation:** Each time a user posts/shares content, our chat bot uses a webhook to get a call. This chat bot then uses the same backend AI as content consumption to determine if the new post by the user contains any unverified information. If so, the user is notified and can choose to either take it down or let it exist.

### How we built it
Our chrome-extension is built using javascript that uses advanced web scraping techniques to extract links, posts, and images. This is then sent to an AI. The AI is a collection of API calls that we collectively process to produce a single "trust" factor. The APIs include Microsoft's cognitive services such as image analysis, text analysis, bing web search, Twitter's search API and Google's Safe Browsing API. The backend is written in Python and hosted on Heroku. The chatbot was built using Facebook's wit.ai

### Challenges we ran into
Web scraping Facebook was one of the earliest challenges we faced. Most DOM elements in Facebook have div ids that constantly change, making them difficult to keep track of. Another challenge was building an AI that knows the difference between a fact and an opinion so that we do not flag opinions as false, since only facts can be false. Lastly, integrating all these different services, in different languages together using a single web server was a huge challenge.

### Accomplishments that we're proud of
All of us were new to Javascript so we all picked up a new language this weekend. We are proud that we could successfully web scrape Facebook which uses a lot of techniques to prevent people from doing so. Finally, the flawless integration we were able to create between these different services really made us feel accomplished.

### What we learned
All concepts used here were new to us. Two people on our time are first-time hackathon-ers and learned completely new technologies in the span of 36hrs. We learned Javascript, Python, flask servers and AI services.

### What's next for FiB
Hopefully this can be better integrated with Facebook and then be adopted by other social media platforms to make sure we stop believing in lies.

### Built With
javascript
python
bing
microsoft-cognitive-services
heroku
facebook
twitter
wit.ai
ibm-watson
bluemix
flask
