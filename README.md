# political-sentiment-analysis
Pan(dem)ic Reading: Sentiment Analysis of Political Nonfiction at the Seattle Public Library 


Charles Dixon
ENG286H1F
6 December 2022
*Pan(dem)ic Reading: Sentiment Analysis of Political Nonfiction at the Seattle Public Library*

**Accessible via Jupyter Hub**; **For Figures, see full docx file**

When COVID-19 first spread globally, questions of crisis and existential uncertainty rose to the top of people’s agenda. So many readers turned to the gloomy worlds of dystopian and post-apocalyptic fiction as a method to situate the pandemic into perspective, where fictional representation of crisis gave a kind of familiarity to the real-life situation of COVID-19 (Shwetz). It was one thing for us all to immerse ourselves in novels remarkably devastating in content, but another to realize how global catastrophes impact the normally taken-for-granted social, political, and cultural structures. As researcher Katherine Shwetz noted, “[c]ontagious diseases […] remind us that the social and cultural boundaries we use to structure society are fragile and porous, not stable and impermeable.” Living in moments of crisis forces one to understand the significance of crises altogether—of not only superficially realizing a virus’s impact on everyday life but realizing its influence on the social and political organization of nations at large. 										
    
Following Shwetz’s observations on “negative” fiction consumption at the beginning of pandemic, my project aims to observe the Seattle Public Library’s checkout dataset to determine the sentiment of nonfiction checkouts in April 2020. Analyzing the library’s checked-out book titles, I intend to apply the “negative” sentiment associated with fiction and shift focus to political nonfiction book titles. My experiment observes if, under “negative” catastrophic circumstances, people read an increased amount of “negative” sounding nonfiction. The reason for particularly targeting political books is to get a sense of the totality of readers’ mindsets in a particular community. That is, if a virus’s gloomy proximity makes one conscious of a nation’s hegemony, such as the political organization of a country, how might the readership pertaining to such subjects be affected to an extent that its polarizing majority appears sentimentally negative?  My hypothesis follows that most book titles checked out from the library’s Nonfiction/Politics category are “negative” sounding under TextBlob’s sentiment analysis feature. Noting the historical context of the library’s dataset, I predict my hypothesis to be correct in that negative polarity scores from political book titles will outweigh the positive. Overall, the usefulness of my experiment will provide a general—albeit, due to the limits of TextBlob’s vocabulary, not fully objective—overview of the mindset of readers during times of crisis. 													
    
My rationale for using the library’s dataset stemmed from curiosity about Seattle’s readership at the start of the pandemic. The reason for specifically focusing on political non-fiction was because of how close the collected data is to the national Black Lives Matter protests of June 2020. By paying attention to political readership, my motive was to observe how political thought trended over time, and how much “negative” sounding titles seduced readers’ checkout motives. Having access to the library’s June 2020 dataset, I additionally drew a small comparison between April and June’s political nonfiction checkouts based on sentimental scores to see if negativity either increased or decreased over the two months. A limitation in the datasets, however, were how they determined the genre of each title: some books may have been political but were nevertheless categorized differently.  The dataset simply does not provide a full range of each nonfiction book’s content with all the minute intertextual differences; if it did, I believe the number of title rows would be higher than 268, given how broad the political nature of a book can be.											
    
The methods employed within my project’s code made use of Pandas and TextBlob Python libraries. Pandas were imported to sufficiently organize the library datasets into the needed columns, namely, the “Subjects,” “Title,” and “Checkouts.” From there, I specified the exact “Subjects”-type to analyze political nonfiction, which the library categorized under the subject, “Nonfiction, Politics” (Figure 1). Once I had a selection of all “Nonfiction, [Political]” books, I then reduced the chart to only titles (Figure 2) and created a series of lists and for loops to integrate each row into a TextBlob argument. The result, in turn, calculated the sentiment polarity of each title, where I then plotted raw and rolling curve charts, of every 10, 50, and 100 titles, to analyze the sentiment trends of 268 books (Figure 3). 					
    
The sentiment results were both neutral and underwhelming in TextBlob’s ability to determine the polarity of words. Although most titles fell under negative polarity, a large portion of them were sentimentally neutral, containing no positive or negative attributes in the titles’ syntax. A reason for this could be that TextBlob does not contain a high enough lexicon to include some of the ‘political’ words in the books’ titles, such as Towards Collective Liberation: Anti-Racist Organizing, Feminist Praxis, and Movement Building Strategy, which contains a large sum of positive sounding political words (“Collective,” “Liberation”, “Praxis”) but fell under a zero-polarity score. Another issue was the differences between qualitative and quantitative results: although negative sentiments were quantitatively dominant, positive sentiments qualitatively undermined their scores. The difference in range pushed against my hypothesis, where positive sentiments contained a maximum score of 0.8, whereas negative sentiments were -0.4—an unequal 1.2-point polarity difference in the April dataset. Even if the plotted curve contained a larger sum of negative sentiments, the polarity score for positive titles was higher in range than if a negative title was in its negative range, even within the rolling polarity curves. Interestingly, the June 2020 negative and positive sentiment increased to -0.7 and 1.0 out of a larger total checkout number of 320, indicating somewhat of a trend from April to June. It seems that in times of crisis readership increased to higher positivity in quality and higher negativity in quantity. Though my hypothesis did predict a bigger number of negative checkouts, an equal number of qualitative and quantitative negative scores would be more beneficial in determining the mindset of readers, as it would firmly tie the quantity of checkouts with the titles’ negative sounding political subject matter together. 					
    
The biggest crux was methodologically limiting the experiment to only titles to detect readers’ attitudes within global crises. Title sentiments may seem like a simple way to understand a reader’s motive, but the correlation between a book’s title, its content, and the number of checkouts remains unclear. One way I tried solidifying the relationship between sentiment titles and subject matter was through additional sentiment analysis of the most “positive” title’s summary blurb—The Great Convergence: Asia, the West, and the Logic of One World—to see if it remained positive. Indeed, it did, but TextBlob’s lexicon still gave ambivalent results: overtly positive words like “optimistic” had an unreasonable polarity score of zero (Figure 4). Based purely on title sentiments, a broader category of political nonfiction checkouts, a higher TextBlob lexicon, and a larger dataset of multiple comparable months would ultimately allow the experiment more accurate results.  


Works Cited
Doubek, James, and Christianna Silva. “Fascism Scholar Says U.S. Is ‘Losing Its Democratic Status’.” NPR, 6 Sept. 2020, www.npr.org/2020/09/06/910320018/fascism-scholar-says-u-s-is-losing-its-democratic-status. Accessed 5 December 2022.
Shwetz, Katherine. “Apocalyptic fiction helps us deal with the anxiety of the coronavirus pandemic.” The Conversation, 18 March 2020, www.theconversation.com/apocalyptic-fiction-helps-us-deal-with-the-anxiety-of-the-coronavirus-pandemic-133682. Accessed 5 December 2022.
Zacharek, Stephanie. “2020 Tested Us Beyond Measure. Where Do We Go From Here?” Time, 5 December 2020. www.time.com/5917394/2020-in-review/. Accessed 5 December 2022.

