
# Possible Improvements and Drawbacks

This project seems to be quite moderate, and there can always be some room for improvements.

Some possible improvements and drawbacks are:
- The dataset contains just the genres, which has be used for grouping the movies. The dataset could also contain the name of the actors, actresses, directors, etc.
They could also become an important criteria for grouping.
- The datasets does not contain any separate information about whether the user has seen any movie or not, which made us assume that a user has seen a movie if and only if 
he/she has rated it. If we had more information about the user (like some reviews, which could have been decoded using NLP), we could have made the recommendations even better.
- This code uses a basic unsupervised algorithm for clustering the movies, and results are actually satisfiable. This result could probably have been even better
that too with somewhat less time complexity if the specialised libraries like surprise or lenskit would have been used.
- The number of tags in the tags.csv file is quite large as compared to the number of movies (approx. 1600 tags for 9750 movies, leading us to hardly 3-10 movies per tag).
Thus the tags dataset could not be used effectively.
- The list of top rated movies will always show the movies from the 1990's, because they have more views, and the views/(no. of years) ratio also didn't make much of a difference. 
For getting the latest hits, we most probably need to fix a timeline. Some possible solution can be adding more weights to the latest movies as compared to the previous ones.
Or we need some extra information like no. of views/or no. of tickets sold/no. of reviews per day/week/month/year for each movie when it was released.
- The movie titles contain some small errors like "The Matrix" is wrongly written as "Matrix, The". Thus in these cases, upon entering the movie name, 
we might get some "wrong movie name" message.
