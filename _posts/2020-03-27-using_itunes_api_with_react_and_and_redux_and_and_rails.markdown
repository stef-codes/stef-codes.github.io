---
layout: post
title:      "Using iTunes API with React && Redux && Rails"
date:       2020-03-27 22:38:19 +0000
permalink:  using_itunes_api_with_react_and_and_redux_and_and_rails
---


For my final Flatiron Project, I created a Music Journal. You can save songs and add them to your journal with the feeling and other text associated with that song. For example, "I remember this song from High School". Expanding this project may include more music details for Music Producers or Songwriters to have collections that help them electronically save notes about songs, including their own.

While creating this project, I realized Redux is tough and not using Redux is tough. This paradox came when using the iTunes Search API.

This data comes nicely formatted in JSON and you don't need a key to access. So, that eliminated another step

In order to get this data I needed to fetch. I didn't use axios, though I may in the future. For my project, I needed songs and I had to give the API a search term. I could hard code the media type as music. And I needed to get the search term from user input. I fetched the data in my handleSubmit function after a user inputted the term they wanted to search.

The tricky part.

I now have search results. However, I'm not going to hold them in state. But, I need to do 3 things:

1. Display the search results on the page.
2. Display more details of the chosen song on a view page.
3. Add that song to a list of saved songs, if chosen.


To accomplish this, I have to bypass the Redux and rely on React within the application.

I took the search results from the fetch and pass those results to a Song Item component to hold the details of the song.

I display the Song Title and Image through the SongItem component. This addresses: 1. Display the search results on the page.

I then send the same song information as state to a new path that will address: 2.Display more details of the chosen song on a view page. That path goes to the SongView Component. This is accomplished through the Routes.

Moving to #3, the SongView component displays the songs information and a button to add the song to the database and save it to the Redux store.

And once the song is added the user is sent to the '/songs' path to see all of the songs saved to the database, including the new song that has just been created.

So, that's all three accomplished:

1. Display the search results on the page.
2. Display more details of the chosen song on a view page.
3. Add that song to a list of saved songs, if chosen.

Hopefully, this is helpful for someone else looking to integrate these technologies and use an external API while understanding what should be stored with Redux as global state.
