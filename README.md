# StoryPromptGen

This is the tool I made to summerize story texts, the LLM's don't get it perfect so you will have to do manual checking / cleaning and adjustments according to how models behave on the dataset.
Originally the idea was to accompany this tool with a specialized model to write the prompts but this was very expensive to make due to the context needed and was proven unneccesary.

This public release is a newer version of that original idea that I used in practise for the [BookAdventures](https://huggingface.co/KoboldAI/Llama-3.1-8B-BookAdventures) model. Instead of using a specialized model it will ask for a summary and then use a second turn to rewrite this summary into a prompt. To do this multiple handwritten conversion are embedded in the script based on public domain works taken from gutenberg. In these examples intentionally nothing is mentioned about the author and book title (This can however happen if you are not careful, especially on autobiography's, verify the data afterwards).

To keep it format agnostic the tool expects cleaned plain text files each containing one work, (or chapter if you wish to try this chapter based) it will then create a new folder with the prompts. I also bundled seperate files to allow converting these into ShareGPT and other formats.

This tool should be used with KoboldCpp (or compatible software) and was tested on Llama3.1-8B-Instruct

# License
No formal fancy license, feel free to use it for whatever you want but if you make a tool based on this method or use it to produce your dataset please credit my work.
