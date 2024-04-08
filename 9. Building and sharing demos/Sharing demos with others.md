# Sharing demos with others

Gradio demos can be shared in two ways: 
- using a temporary share link or
- permanent hosting on Spaces.

We’ll cover both of these approaches shortly. But before you share your demo, you may want to polish it up 💅

## Polishing your Gradio demo
![](https://huggingface.co/datasets/huggingface-course/documentation-images/resolve/main/en/chapter9/gradio-demo-overview.png)

To add additional content to your demo, the **Interface class** supports some optional parameters:

- **title:** appears above the input and output components.
- **description:** (in text, Markdown, or HTML) which appears above the input and output components and below the title.
- **article:** (in text, Markdown, or HTML) explaining the interface. If provided, it appears below the input and output components.
- **theme:** don’t like the default colors? Set the theme to use one of default, **huggingface, grass, peach**. You can also add the **dark-** prefix,
- e.g. dark-peach for dark theme (or just dark for the default dark theme).
- **examples:** to make your demo way easier to use, you can provide some example inputs for the function. These appear below the UI components and can be used to populate the interface.
These should be provided as a nested list, in which the outer list consists of samples and each inner list consists of an input corresponding to each input component.
- **live:** if you want to make your demo “live”, meaning that your model reruns every time the input changes, you can set **live=True**. This makes sense to use with quick models.

- Using the options above, we end up with a more complete interface. Run the code below so you can chat with Rick and Morty:

```python
title = "Ask Rick a Question"
description = """
The bot was trained to answer questions based on Rick and Morty dialogues. Ask Rick anything!
<img src="https://huggingface.co/spaces/course-demos/Rick_and_Morty_QA/resolve/main/rick.png" width=200px>
"""

article = "Check out [the original Rick and Morty Bot](https://huggingface.co/spaces/kingabzpro/Rick_and_Morty_Bot) that this demo is based off of."

gr.Interface(
    fn=predict,
    inputs="textbox",
    outputs="text",
    title=title,
    description=description,
    article=article,
    examples=[["What are you doing?"], ["Where should we time travel to?"]],
).launch()
```

## Sharing your demo with temporary links

 Interfaces can be easily shared publicly by setting share=True in the launch() method:

 ```python
gr.Interface(classify_image, "image", "label").launch(share=True)
```

This generates a public, shareable link that you can send to anybody! When you send this link, the user on the other side can try out the model in their browser for up to 72 hours. 
Because the processing happens on your device (as long as your device stays on!), you don’t have to worry about packaging any dependencies. 
If you set share=False (the default), only a local link is created.

## Hosting your demo on Hugging Face Spaces
Hugging Face Spaces provides the infrastructure to permanently host your Gradio model on the internet, for free! Spaces allows you to create and push to a (public or private) repo, where your Gradio interface code will exist in an app.py file.

If you’re working out of a Google Colab notebook, a share link is always automatically created. It usually looks something like this: XXXXX.gradio.app.
