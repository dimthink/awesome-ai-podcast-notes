---
title: "AutoGen FULL Tutorial with Python (Step-By-Step) 🤯 Build AI Agent Teams! - 结构化文稿"
channel: "Matthew Berman"
published: "2023-10-10"
source_url: "https://www.youtube.com/watch?v=V2qZ_lgxTzg"
video_id: "V2qZ_lgxTzg"
variant: "structured"
---

# AutoGen FULL Tutorial with Python (Step-By-Step) 🤯 Build AI Agent Teams! - 结构化文稿

- **Channel:** Matthew Berman
- **Published:** 2023-10-10
- **Source:** https://www.youtube.com/watch?v=V2qZ_lgxTzg
- **Main:** [AutoGen FULL Tutorial with Python (Step-By-Step) 🤯 Build AI Agent Teams!](2023-10-10-autogen-full-tutorial-with-python-(step-by-step)-🤯-build-ai-agent-teams!-V2qZ_lgxTzg.md)

# AutoGen Full Tutorial with Python: Build AI Agent Teams Step-by-Step

I am absolutely obsessed with AutoGen. It is the coolest piece of AI technology that I've seen since I first saw ChatGPT. I already created a beginner tutorial video and overview of AutoGen and its capabilities, but now I'm going to give you a more advanced tutorial. We're going to set it up on our computer, and I'm going to walk you through it step by step. Not only that, I have plans for a series of videos about AutoGen. If there are any AutoGen-related topics you want to see, let me know in the comments. On that note, let's go.

As a reminder, **AutoGen allows you to set up multiple artificial intelligence agents that work together to accomplish any task you give them**. They can use tools, they can code, they can execute code – it is phenomenal. Think of it like ChatGPT + Code Interpreter + plugins, but fully customizable, and you can drop it into your application you're building. So, I'm going to show you how to actually use the code locally. This will be a little bit of a slower-paced video because I am going to walk you through step by step, each line of code that I'm creating.

## Prerequisites

You’ll need just a few things to get this to work:

- **Visual Studio Code** (you can use any code editor you want)
- **Anaconda** installed
- **An OpenAI account** (I'm still working on getting an open-source model set up, so we'll continue using OpenAI for now)
## Setting Up the Project

1. **Open Visual Studio Code** and create a new file. Once you have that new file created, go ahead and click **Save**. I already created a folder called `autogen`. If you don't already have a folder specific for this project, go ahead and create one. I'm going to rename this file to `app.py` and save it.
1. **Open the terminal** by clicking the little button in the top right of Visual Studio Code. Next, we'll create a new Conda environment to help manage all our Python versions and modules. You should already have Anaconda installed – if not, install it (just Google how to do it if you don't know how).
Run the following command in the terminal:

CODEBLOCK*0python*

import autogen

CODEBLOCK*1python*

config*list = [*

{

'model': 'gpt-3.5-turbo-16k',   # I would recommend using GPT-4, but for showing the code we don't need it.

'api*key': 'your-api-key-here'  # Replace with your actual OpenAI API key*

}

]

CODEBLOCK*2python*

llm*config = {*

"request*timeout": 600,   # Kills the request after a certain time if OpenAI's API isn't responding*

"seed": 42,               # For caching – once you run a task, it caches the response, saving money and time

"config*list": config*list,

"temperature": 0          # 0 = less creative, deterministic responses (good for coding)

}

CODEBLOCK*3python*

assistant = autogen.AssistantAgent(

name="assistant",

llm*config=llm*config

)

CODEBLOCK*4python*

user*proxy = autogen.UserProxyAgent(*

name="user*proxy",*

human*input*mode="TERMINATE",   # Options: "ALWAYS", "TERMINATE", "NEVER"

max*consecutive*auto*reply=10,  # Prevents infinite loops and high costs*

is*termination*msg=lambda x: x.get("content", "") and x.get("content", "").rstrip().endswith("TERMINATE"),

code*execution*config={"work*dir": "web"},   # Files will be written to a "web" subfolder*

llm*config=llm*config,

system*message="""Reply TERMINATE if the task has been solved at full satisfaction.*

Otherwise, reply CONTINUE, or the reason why the task is not solved yet."""

)

CODEBLOCK*5python*

task = """

Give me a summary of this article:

[Paste a random article here]

"""

CODEBLOCK*6python*

user*proxy.initiate*chat(

assistant,

message=task

)

CODEBLOCK*7python*

task = "Write Python code to output numbers 1 to 100 and then store it in a file."

CODEBLOCK*8python*

task = "Write Python code to output numbers 1 to 100 and then store the code in a file."

CODEBLOCK*9python*

task2 = "Change the code in the file you just created to instead output numbers 1 to 200."

user*proxy.initiate*chat(

assistant,

message=task2

)

Also, change `human`*`input`*`mode` to `"NEVER"` for fully automated execution (though be careful with risky code).

**Result**: The assistant updates the file (or creates a new one) to output 1–200. It might not follow directions perfectly if the prompt isn't explicit, but it works for demonstration.

## Final Thoughts

There are many ways to improve this code:

- Store the model and API key as **environment variables** (e.g., in a `.env` file) to avoid committing secrets.
- Move the `llm`*`config`** to a separate file.*
- Organize the code with proper refactoring.
Now you can extend it further: add more agents, experiment with different prompts, play with caching techniques. It's truly incredible. I'm still working on getting an open-source model set up – as soon as I do, I'll publish another video.

If you enjoyed this series and want more AutoGen content, let me know! I'm so excited about it. If you liked this video, please consider giving it a like and subscribing. I'll see you in the next one.
