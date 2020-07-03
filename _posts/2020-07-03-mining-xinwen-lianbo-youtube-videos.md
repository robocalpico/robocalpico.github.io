---
layout: post
title: Mining Xinwen Lianbo Youtube videos
tags: cctv youtube
date: 2020-07-03 15:28 -0400
categories: Posts
---
<blockquote class="blockquote">
  <p class="mb-0"> Xinwen Lianbo is a daily news programme produced by China Central Television, a state broadcaster. It is shown simultaneously by all local TV stations in mainland China, making it one of the world's most-watched programmes. It has been broadcast since 1 January 1978.</p>
  <footer class="blockquote-footer">Wikipedia</footer>
</blockquote>

*one of the world's most-watched programmes* is an understatement. Everyday, 7 to 7:30 PM, billions of families sit together, usually at dinner time, watch the program. It used to be the only multi-media news in China, and still is for many even today. To put it mildly, it shapes the mind and perception of many generations in its 40 years of broadcasting.

On the other hand, CCTV, the organization that produces Xinwen Lianbo (Xinwen for short), has a Youtube account, and has been uploading every episode of the program for a while. Since Youtube has API to fetch metadata of its videos, I figure it would be fun to do some basic data analysis to this influential show.

CCTV nicely keep all Xinwen episodes into one playlist, making data fetch easy. Once I pulled them down I found there are only **484** videos (as of 6/15/2020). It ranges from **January 2019** to **June 2020**. It seems either CCTV only started uploading videos in 2019, or it has been actively removing outdated ones.

For each video, Youtube provides the video title, url, tags, and stats about view, comment and likes/dislikes.

The thing that interests me the most, is how frequent the program mentions their top leader Xi in its title? I know it might be a weird starting point, but it just somehow grew on me.

A simple string comparison shows that between January 2019 and June 2020, **81.18%** of time the program mentions the name of the supreme leader in the title. It roughly translates to **6 days a week**. I then further break down the count to each  month:

<figure><img src="{{ "/assets/img/yt_cctv/xi_mention_by_month.png" | relative_url }}" class="img-fluid" alt="Xi mentions by month"></figure>

Visually the mentions per month suddenly surged at June 2019, and stayed at the higher level than previous since then. Looking thru the titles didn’t give me clear ideas of why.

Then I take a look at how frequent some common topics are mentioned:

<figure><img src="{{ "/assets/img/yt_cctv/common_topics.png" | relative_url }}" class="img-fluid" alt="Common topics"></figure>

So ‘政治’ (politics) and ‘经济’ (economy) seem to be the major topics, and also the two things that matter the most? Wonder how headlines of other news media compare to it.

I also try to count the mentions of common actions or generic events:

<figure><img src="{{ "/assets/img/yt_cctv/common_actions.png" | relative_url }}" class="img-fluid" alt="Common actions"></figure>

The top 3 most frequent actions (host, hold, speak) all relates to having meetings. I guess that speaks of the nature of Xinwen: it is about communicating all the meetings that higher leaders have to their people. On the other hand, ‘meeting’ (会见) someone is much higher than ‘visit’ (访问) someone. Does it indicate the increasing influence of Xi globally as more people come to meet him instead the other way around? Again maybe more older data allows us to look into more.

Finally a quick peek on view and comment stat. On average, one single episode gets **41k** views, although this number should only increase over time. Here are the top ranked of most viewed ones:

<figure><img src="{{ "/assets/img/yt_cctv/top_watched.png" | relative_url }}" class="img-fluid" alt="Common actions"></figure>

**150k** views is not impressive at all by Youtube standard ([this Chinese reality show episode](https://www.youtube.com/watch?v=Vn-NLEdsylw) uploaded 1 month ago gets 1M view). These top watched are all big events: the funeral of a prominent political figure, the celebration of 70th anniversary, Xi visiting Russia and NK, and the 70th anniversary parade. Why a funeral triumphs the big 70th anniversary? It certainly came out 3 months earlier, but this might be something you can explore.

CCTV always disables the comment option for Xinwen videos, but surprisingly, 4 among 484 videos have comments:

<figure><img src="{{ "/assets/img/yt_cctv/comment_episodes.png" | relative_url }}" class="img-fluid" alt="Comment episodes"></figure>

They don’t look like correlate with each other, so it might just be that whoever uploaded the video being careless and forgot to turn off comments? Anyway, it definitely got audience excited, most of whom left comments of being proud or happy of seeing China rising as a strong power in the world:

<figure><img src="{{ "/assets/img/yt_cctv/comment_screenshot.png" | relative_url }}" class="img-fluid" alt="Comment screenshot"></figure>

I hope the third user Chandler Bing won't be disappointed when he/she know the fact that enabling comments on Xinwen videos might be just an unfortunate accident.

Hope you find it interesting like I did. I might have a part-2 post with more analysis later on. What are the other things you think worth looking into? More importantly, does anyone know a way to get the data for older episodes?