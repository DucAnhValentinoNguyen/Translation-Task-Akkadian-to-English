# Translation-Task-Akkadian-to-English
This is a kaggle competition: https://www.kaggle.com/competitions/deep-past-initiative-machine-translation.

A translation system for Old Assyrian: decode the everyday business records of ancient Assyrian merchants, using 8,000 cuneiform texts.

Four thousand years ago, Assyrian merchants left behind one of the world’s richest archives of everyday and commercial life. Tens of thousands of clay tablets record debts settled, caravans dispatched, and discuss day-to-day family matters. This woule be one of the largest untranslated archive of the ancient world. 

### Goal: 
neural machine-translation models that convert transliterated Akkadian into English  

### Context and Challenges:
The challenge: Akkadian is a low-resource, morphologically complex language where a single word can encode what takes multiple words in English. Standard architectures built for modern, data-rich languages fail here.

Context: Old Assyrian—the dialect used on these tablets—is an early form of Akkadian, the oldest documented Semitic language - bronze Age texts from museum collections for over a century. Nearly 23,000 tablets survive documenting the Old Assyrian trading networks that connected Mesopotamia to Anatolia. Only half have been translated, and less than a dozen scholars in the world are specialized to read the rest. These aren’t the polished classics of Greece and Rome, curated and copied by scribes who chose whose voices survived. These are unfiltered, straight from the people who wrote them: letters, invoices and contracts written on clay by ancient merchants and their families. They’re the Instagram stories of the Bronze Age: mundane, immediate, and breathtakingly real.

### Dataset:
(from kaggle)
By far the biggest challenge in working with Akkadian / Old Assyrian texts is dealing with the formatting issues - the format of text in transliteration poses challenges at each step of the ML workflow, from tokenization to the transformation and embedding process.

To mitigate these issues with following information and suggestions in handling the different formatting challenges in both the transliterated and translated texts:
+ Texts in Transliteration
+ Modern Scribal Notations

### Evaluation:

Evaluated by the Geometric Mean of the BLEU and the chrF++ scores, with each score's sufficient statistics being aggregated across the entire corpus (that is, each score is a micro-average).
Reference:
+ SacreBLEU library https://github.com/mjpost/sacrebleu/ for implementation details.
+ A notebook implementing the metric on Kaggle: Geometric Mean of BLEU and chrF++ (https://www.kaggle.com/code/metric/dpi-bleu-chrf).


### Submission File:
For each id in the test set: predict an English translation of the associated Akkadian transliteration. Each translation should comprise a single sentence. The file should contain a header and have the following format:

id,translation
0,Thus Kanesh, say to the -payers, our messenger, every single colony, and the...
1,In the letter of the City (it is written): From this day on, whoever buys meteoric...
2,As soon as you have heard our letter, who(ever) over there has either sold it to...
3,Send a copy of (this) letter of ours to every single colony and to all the trading...
...




