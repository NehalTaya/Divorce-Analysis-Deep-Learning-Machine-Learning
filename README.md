# DIVORCE DATASET ANALYSIS

**BACKGROUND**

Using the divorce data to  determine the factors that influence divorce

**DATASET**

This data is from the University of California Irvine machine learning dataset repository

**Divorce dataset**

Reference: https://archive.ics.uci.edu/ml/datasets/Divorce+Predictors+data+set

Articles which discuss the dataset:
https://medium.com/analytics-vidhya/a-logistic-model-for-predicting-divorce-rates-amongcouples-implemented-using-the-statsmodel-api-763e03d29d68

https://dergipark.org.tr/en/pub/nevsosbilen/issue/46568/549416

The divorce dataset from the Machine Learning Repository at University of California Irvine 
contains 170 responses to a survey. Of the 170 respondents, 84 (49%) were divorced, 86 (51%) 
remained married. They were asked 54 questions and the answers to the questions were 
collected on a 5-point scale (0-4):

0 Never

1 Seldom

2 Average

3 Frequently

4 Always

The questions were:
1. If one of us apologizes when our discussion deteriorates, the discussion ends. 
2. I know we can ignore our differences, even if things get hard sometimes. 
3. When we need it, we can take our discussions with my spouse from the beginning and correct 
it. 
4. When I discuss with my spouse, to contact him will eventually work. 
5. The time I spent with my wife is special for us. 
6. We don't have time at home as partners. 
7. We are like two strangers who share the same environment at home rather than family. 
8. I enjoy our holidays with my wife. 
9. I enjoy traveling with my wife. 
10. Most of our goals are common to my spouse. 
11. I think that one day in the future, when I look back, I see that my spouse and I have been in 
harmony with each other. 
12. My spouse and I have similar values in terms of personal freedom. 
13. My spouse and I have similar sense of entertainment. 
14. Most of our goals for people (children, friends, etc.) are the same. 
15. Our dreams with my spouse are similar and harmonious. 
16. We're compatible with my spouse about what love should be. 
17. We share the same views about being happy in our life with my spouse 
18. My spouse and I have similar ideas about how marriage should be
19. My spouse and I have similar ideas about how roles should be in marriage 
20. My spouse and I have similar values in trust. 
21. I know exactly what my wife likes. 
22. I know how my spouse wants to be taken care of when she/he sick. 
23. I know my spouse's favorite food. 
24. I can tell you what kind of stress my spouse is facing in her/his life. 
25. I have knowledge of my spouse's inner world. 
26. I know my spouse's basic anxieties. 
27. I know what my spouse's current sources of stress are. 
28. I know my spouse's hopes and wishes. 
29. I know my spouse very well. 
30. I know my spouse's friends and their social relationships. 
31. I feel aggressive when I argue with my spouse. 
32. When discussing with my spouse, I usually use expressions such as ‘you always’ or ‘you 
never’ . 
33. I can use negative statements about my spouse's personality during our discussions. 
34. I can use offensive expressions during our discussions. 
35. I can insult my spouse during our discussions. 
36. I can be humiliating when we discussions.
37. My discussion with my spouse is not calm. 
38. I hate my spouse's way of open a subject. 
39. Our discussions often occur suddenly. 
40. We're just starting a discussion before I know what's going on. 
41. When I talk to my spouse about something, my calm suddenly breaks. 
42. When I argue with my spouse, ı only go out and I don't say a word. 
43. I mostly stay silent to calm the environment a little bit. 
44. Sometimes I think it's good for me to leave home for a while. 
45. I'd rather stay silent than discuss with my spouse. 
46. Even if I'm right in the discussion, I stay silent to hurt my spouse. 
47. When I discuss with my spouse, I stay silent because I am afraid of not being able to control 
my anger. 
48. I feel right in our discussions. 
49. I have nothing to do with what I've been accused of. 
50. I'm not actually the one who's guilty about what I'm accused of. 
51. I'm not the one who's wrong about problems at home. 
52. I wouldn't hesitate to tell my spouse about her/his inadequacy. 
53. When I discuss, I remind my spouse of her/his inadequacy. 
54. I'm not afraid to tell my spouse about her/his incompetence

**VIF ANALYSIS**

![image](https://user-images.githubusercontent.com/100436462/221028442-294d7048-822c-4511-bc0c-e73443a03de1.png)

![image](https://user-images.githubusercontent.com/100436462/221028655-dc94eca5-3418-4073-bbee-15ae6f44e65d.png)

![image](https://user-images.githubusercontent.com/100436462/221028728-4b9990ef-0944-4ed0-948d-a5f38add96da.png)

**Neural network  with Binary Output Class using the Nine Attributes (Atr) from the VIF analysis and all data points**

![image](https://user-images.githubusercontent.com/100436462/221028862-437e375f-690e-435c-9f36-1a7a54366414.png)

![image](https://user-images.githubusercontent.com/100436462/221029067-4dcea0ae-5c0b-48cf-9473-9de57e0d6a9b.png)

![image](https://user-images.githubusercontent.com/100436462/221029289-9d6ade2d-c2cd-4b3b-9d1e-3d1095e9c908.png)

**Third Neural Network with Binary Output Class using the Attributes  Atr7, Atr43, Atr46, At48, Atr52**

![image](https://user-images.githubusercontent.com/100436462/221029521-ba3eea30-fe75-4e2a-8674-8547eab72917.png)

![image](https://user-images.githubusercontent.com/100436462/221029595-0d0c08a0-aad1-49d2-bb19-29d16662737c.png)

![image](https://user-images.githubusercontent.com/100436462/221029642-7f965b04-49b1-41df-a401-2cca5a0cf612.png)

![image](https://user-images.githubusercontent.com/100436462/221029725-6de1bbc5-0195-4eb8-a99c-8032d4db7d14.png)

**CONCLUSION**

Neural Network 3 with Class as output variable and Atr7, Atr43, Atr46, At48, Atr52 as input variable has very high prediction accuracy as compared to Neural Network 2 with all the attributes with VIF <9 as input variables 

Thus only 5 attributes out of 54 help in predicting divorce event and they are as follows:

These 5 questions in order of impact are highlighted below:

1.We are like two strangers who share the same environment at home rather than family. Divorced couples were 275x more likely to reply affirmatively to this question.

2.Even if I’m right in the discussion, I stay silent to hurt my spouse. Divorced couples were 0.54x more likely to reply affirmatively to this question.

3.I mostly stay silent to calm the environment a little bit. Divorced couples were 3.8x more likely to reply affirmatively to this question.

4.I feel right in our discussions. Divorced couples were 3.0x more likely to reply affirmatively to this question.

5.I wouldn’t hesitate to tell my spouse about her/his inadequacy. Divorced couples were 3.0x more likely to reply affirmatively to this question.




