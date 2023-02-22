## Introduction
The project is about finding the most popular content category for a social media company called "Social Buzz".
I will be using three datasets to achieve this objective. The datasets are:
* Content
* Reaction
* ReactionTypes
More details on the datasets:
### Content
ID: Unique ID of the content that was uploaded (automatically generated)

User ID: Unique ID of a user that exists in the User table

Type: A string detailing the type of content that was uploaded

Category: A string detailing the category that this content is relevant to

URL: Link to the location where this content is stored

### Reaction
Content ID: Unique ID of a piece of content that was uploaded

User ID: Unique ID of a user that exists in the User table who reacted to this piece of content

Type: A string detailing the type of reaction this user gave

Datetime: The date and time of this reaction

### ReactionTypes
Type: A string detailing the type of reaction this user gave

Sentiment: A string detailing whether this type of reaction is considered as positive, negative or neutral

Score: This is a number calculated by Social Buzz that quantifies how “popular” each reaction is. A reaction type with a higher score
should be considered as a more popular reaction.