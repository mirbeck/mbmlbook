The original dataset was modified in the following way:

• Removed 18 movies (out of the 9K) which have the following genres: "(no genres listed)"
	○ Note that these movies are not special in any way. For instance, one of them is Grandma (2015), which, when you check in IMDB, has genres Comedy, Drama
	○ Also removed the entries with these movies in the ratings dataset.
• Removed some extra spaces (5, in particular) which were in the way of the feature parser
• Removed item features for the following two movies, since they don't have a year of release. Stranger things only had one rating in the rating dataset (removed), Women of '69 didn't have any
	○ 164979::Women of '69, Unboxed::Documentary
	○ 162376::Stranger Things::Drama
• Removed 108548::Big Bang Theory, The (2007-)::Comedy since it doesn't have a fixed year. It only had one rating in the ratings dataset (removed).
• Multiplied the ratings by 2. So the original values that varied from 0.5 to 5 are now 1 to 10. Goes well with the "star" explanation. 
• Converted the commas in the .csv to ";" (but not in the movie names). This makes parsing later easier. 