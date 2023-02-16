# Podcast Summarizer
Podcast are a wealth of information, but they tend to have tons of episodes that are upwards of 1-2 hours per. This Google Colab will take a given podcast feed and will create a transcript and "good enough" summary for each audio episode for free! There is also an option to use OpenAI's GPT3, which does charge, but is super cheap.

## Details
Each episode will get a text file in the transcription folder that will contain:

*   Speaker identification (optional)
*   Using Speach to Text transcribe what was said by each speaker. Example: 
  > 0:00:00.000-0:00:33.960> SPEAKER_01:  Welcome to the Profitable Farmer podcast, where we share stories and tips to help you run a better farming business and create your very own freedom farm. If you're looking to work smarter and not harder in your farm business, welcome, you're in the right place. .... 
*   Summerize the episode
  > FarmTender was founded in March 2012, but the backstory of its founder goes back further. He grew up on a family farm in the Wimmera and made the decision to move away from primary production so he could pursue something new. He had an interest in building databases and the internet, and was brave enough to leave something that offered certainty to go and try something else. After trying a few different things, he heard a farmer at a field day asking why he couldn't sell his products online. This gave him the idea for FarmTender, and he worked with a developer to get it up and running. It was a tough process, but he had a database of 2000 members to help him get started. With lots of cold calling and content creation, FarmTender has grown significantly since then....

### Note About The Summaries
This project is aiming for good enough to quickly read through.

## FAQ

### Does my computer need a graphics card?
NO! This runs in the cloud and does NOT require your personal machine to have a graphics card.

### Where is the output located?
gDrive -> My Drive -> Summarize_Podcasts -> PODCAST_NAME_HERE -> Transcript <br>

In you gDrive there will be a directory called "Summarize_Podcasts". When you run this notebook for a podcast a directory will be created in this folder by that name. Podcast "Reply All" will be "replyall". In there you will find the "transcript" folder where you will find the transcript and summary.

### How long does this need to run?
* In testing, for a 1 hour podcast episode it takes around 20-25 minutes.

### Which Runtime Type?
You will need to use a **GPU** Runtime. In order to select a runtime, on the menu: 
1. Click “Runtime” -> “Change runtime type”
2. Under "Hardware Accelerator" -> select "GPU" 
3. Click “Save”

### How do I run this?
1. Go to the Required Information section, below, and fill out the forms.
2. Once filled in, on the menu, click “Runtime” -> “Run All”
 * Or you can press "shift + enter" on your keyboard until you get to the end of this document to run each cell.

### Keep this tab open and don't let your computer sleep
Colab, unless on the $50 dollar plan, requires this tab to stay open and that the computer running this tab stays awake while executing

### Uh oh, the runtime shutdown before completing
No need to worry. This code has been setup to pick up where it left off in processing. Just reconnect, with GPU collab. Depending on how long each episode is and how many episodes, this could take a few sessions. 

### Empty gDrive Trash
If you run this a few times, you will need to empty your gdrive trash to free up space. [More information can be found here on how to do that ](https://support.google.com/drive/answer/2375102?hl=en&co=GENIE.Platform%3DDesktop)

### Which languages are supported?
* English
While Whisper does support additional languages, with varying degrees of accuracy, I don't know enough of the various languages to validate if the summarization is even in the "good enough" category. Reach out if you want to help.

### How do I track progress?
After you click the run button, scroll down to the bottom to see the logs to see the progress.
