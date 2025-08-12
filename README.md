# Simple Prompt Art Generation Workflow
This repository consists of an art generation workflow that takes a simple character prompt and art style and transforms them into a cinema-grade visual. I designed this workflow specifically to test out my ability to create a microservice, hooking up this automation to a front-end built in Lovable. Super cool experiment, I learned a ton and I would definitely recommend it to anyone that's considering testing it out!

## Tech Stack:
The Simple Prompt Art Generation workflow runs completely on AI models and JS code, with no other software needed. I'm personally using Perplexity and OpenAI models for this workflow, but if you want to jump on Hugging Face or another AI model site and grab a different image generation model, be my guest.

## The Workflow:
The workflow itself functions in two distinct stages.

### Prompt Generation:
The webhook is used to pull in a response from my front-end web interface, grabbing the simple character prompt and an art style. Because I tried to make my art styles sound cooler on my website, I'm using a JS code block to transform them into actual art styles, then using ChatGPT to enhance the character prompt and a Perplexity search to capture the essence of the requested art style. From there, all the content is combined back into one path.

### Image Generation:
The combined data is run through another ChatGPT prompt to amalgamate the information and create a comprehensive image generation prompt. It's then passed to Dall-E 3 to generate the image, before being sent back to the webhook so that user can grab their generated image!

## Future Improvements:
I'd love to expand this into video generation as well using Veo or a similar model.
