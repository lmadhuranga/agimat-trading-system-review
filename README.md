# Review of the Agimat Trading System

System link: [https://www.agimat-trading-system.com/](https://www.agimat-trading-system.com/)

The [Agimat Trading System 2018](https://www.agimat-trading-system.com/) by Mr. Buchholz repaints a lot and contains mostly freely available MQL indicators, that have been changed a bit, and few others unknown to me.

## Indicators

It comes with the following 9 indicators:

1. "**MEQ/""Maxwells Equations OCC"/"Future Prediction**" indicator

This is the XprofuterDD indicator (https://www.mql5.com/en/code/7558). MEQ has almost the same input names and values as the XprofuterDD. XprofuterDD has two lines. The second line shows the bar body size. The first line is a calculation based on the bar body size. When you apply the Agimat template, for all historical bars the second Xprofuter line will be shown in MEQ and for all live calculated bars the second Xprofuter line will be shown in MEQ which is the bar body size. See a screenshot comparing MEQ and Xprofuter: https://i.imgur.com/sfmqt4u.png .

The calculation for this indicator is a simple for loop with incremental addtion of the last 14-15 body sizes (negative and positve): for(i=shift; i>=lim; i--) {imp=imp + (Close[i] - Open[i])/Point;} , which has nothing to do with the great Maxwells Equations from physics.

MEQ is not a future price predictor and it not trade volume future prediction, it is just a calculation based on past body sizes. When the price drops in a downtrend, MEQ goes high. Being shifted 14 bars to the right, it confirms your bias for counter trending as per Agimat rules.

In this video https://youtu.be/0P3Iiq9onNg?t=550 the Mr. Buchholz tells you that this indicator is not TDI, RSI, MACD or whatever. But he does not tell you that this is the publicly free XprofuterDD indicator and does not teach you what exactly it is.

The MEQ indicator contains several inputs named "NeuralServerPort", "ServerIP", "ServerDNS", "NeuroNetClass", etc, which are irrelevant for the calculations of this indicator.

Repaints: Yes, partly, as explained above.

2. "**AgimatFX2018pro_ConA**", shortly **ConA**

3. "**AgimatFX2018pro_ConB**", shortly **ConB**.

ConA is the "3_Level_ZZ_Semafor" (https://www.mql5.com/en/code/7730), even the input names are the same and most of the input values. Semafor is responsible for the yellow boxes of Agimat.
ConB is reponsible for the black arrows of the yellow boxes. It seems to be a variation of the ZigZag Arrow Indicator, but shown only in the yellow boxes https://www.mql5.com/en/code/13049 . 
Repaints: Yes, both.

4. "**Angular Momentum"/"AAM**".

Currently I do not know what exactly this is. It does not repaint. A previous user commented that it might be "Ang Zad 2CI" https://4xone.com/ang-zad-2ci-mt4-indicator/ . It is similar, but not the same: 2CI is not as smoothed as AAM. Most probably it a simple mechanical (not neural network/AI) calculation that I am not aware of.
Repaints: No.

5. "**Alert**" is the white arrow and makes an alert for a condition that depends on period, deviation step, length and bars. Repaints: Yes (compare past and live white arrows with those in strategy tester)

6. "**PriceLineGrid**" is the SweetSpots.mq4 (http://forex-indicators.net/support-resistance/sweet-spots). It just displays round numbers. Repaints: No.

7. "**HA**" is the standard MQL4 Heiken Ashi indicator. No other indicator bases its calculation upon the Heiken Ashi candles. It is just visual representation and it used for the 4th rule of the Agimat System. Repaints: No.

8. "**BA**" displays the current price. Repaints: No.

9. "**CS**" displays the shortname of the current Symbol. Repaints: No.

So the real deal for this system are the first 4 indicators. The first two are simple free code. The 3rd and 4th indicator seem to be MQL calculations.

## Repainting
Quote from the official website: "Agimat FXtm is a non-repaint Forex trading MT4 indicator, excellent for scalping and swing trades." written below the headline "Is Agimat FX a scam?"(Source: https://web.archive.org/web/20181220122748/https://www.agimat-trading-system.com/ and https://i.imgur.com/cvBjbZv.png). Obviously this is a lie, because MEQ, ConA, ConB and Alert repaint. These indicators are used for 3 of the 4 rules of the system. Some people might even call such behaviour hypocrisy.

## Neural Network (NN)
Haven't seen any evidence of it. There might be a NN. Or not. If we check the indicators: MEQ is not NN. ConA is not NN. ConB and AAM could be a NN, but most probably are not. Indicators 5 to 9 are too simple for NN.
I used a packet sniffer to check whether there is connection to some other servers, but could not find such packets, only standard MT4 packets, which means either there is no connection to a NN or I could not find the NN packets.

## Backtesting
Because most of the indis repaint, you cannot backtest the Agimat signals in a normal open chart. You could use the Strategy Tester. Whether you can really backtest will depend also whether there is actually a Neural Network (not just a claim) and if yes, what are its effects on backtesting.

## Binary Options
On the official website there are claims about trading it with binary options, but actually you will not be given any advise about it, that you can practically use, only Forex. Not to mention that >95% of the binary options brokers are scammers.

## Past Results
The author, Mr. Buchholz, claims 90% success with his system, but does not provide any evidence of past results. Also given the repainting nature of the indcators, past results will be impossible to verify by the user. In some of his comments on this website the author claims that thousands of his clients follow his system and use it successfully, but it is very unlikely that he has asked all of his customers whether they follow his rules and what kind of success they have had.

## Live Trading The System
Having said that, I haven't traded this system, and thus cannot share my experience. There are some traders who have their own rules with this system and claim to have success with it and that might be true. Might be not.

## Impression of the System
The interesting point about this system is trading around the round numbers, waiting for the confirmation of the 2 arrows and the  and AAM which forces you to be patient with reversal trading.

## Main critique arguments and suggestions
- The indicators repaint. Remove claims that they do not repaint and say that they repaint.
- The MEQ indicator is not future prediction. Be honest about that and don't be shy to tell that it is the publicly free XprofuterDD indicator.
- Binary options: provide instruction how to trade it or remove the claim about it.

## Previous critique
Mr. Buchholz does not like negative feedback. There were few previous negative critiques and Mr. Buchholz claimed that the people were fake or the contents were "much out of reality". He assumes that people hate him for his (unproven) success, but fails to acknowledge the critique arguments for his product and that people on this website might not use the name with which they have bought the product.

## Review Publication
This review was sent in 2018 to be published in [Forex Peace Army (FPA)](https://www.forexpeacearmy.com/forex-reviews/13737/agimat-trading-system-trading-software), but FPA have not accepted it yet, although being one of the most detailed reviews of the Agimat system. Thus it is uncensored shared here.

## Conclusion
Make your own conclusion.
