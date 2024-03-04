
# Why might a countdown animation be inaccurate?

When using the time limit feature on the interactive quiz, a countdown animation shows the remaining time before 
the quiz progresses to the next question. However, if the quiz window is inactive or not in focus, the GIF animation 
won't render accurately. When you return to the quiz window, the animation restarts from the beginning, 
failing to reflect the actual remaining time. This is a known limitation.


## Why not update the countdown animation manually instead of using a GIF image?
There are three main reasons:

1) The Slack API imposes restrictions on request frequency. Pushing changes to Slack every second risks hitting the rate limit, causing the app to be unable to update within a specific timeframe.  
2) Network delays can lead to unpredictable behavior. While we could schedule updates every second, delays in network transmission could result in jumps of a second or more in the displayed time.  
3) Preventing race conditions becomes challenging when we lack control over the Slack client's behavior.  

Rather than delivering a buggy application, we opted for slight inconvenience.


## Why do other quizzes not encounter this limitation?
To put it plainly, they are not integrated natively within Slack. As a result, they have complete control over their 
own client environments, making this problem relatively easy to address.
Please inform us if this limitation truly bothers you. If there is significant demand for it, we can develop 
a web-based version without this constraint. The reason we haven't implemented it yet is because it contradicts our 
goal of seamlessly integrating features into your work environment.
