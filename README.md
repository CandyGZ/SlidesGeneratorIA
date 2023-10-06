# SlidesGeneratorIA
Create a bunch of presentation slides just writing the Topic

## Description

This system is designed to automate the process of generating PowerPoint presentations on a given topic. It utilizes the OpenAI API and the python-pptx library to create presentations with slides containing headers and informative content.

## Libraries Used

### 1. openai
   - **Purpose**: To interact with the OpenAI API for generating content.
   - **Usage**: The library allows us to set up an API key, send prompts to the OpenAI GPT-3 model, and retrieve responses.

### 2. json
   - **Purpose**: To handle JSON data.
   - **Usage**: It is used to parse the JSON response from the OpenAI API to extract slide data.

### 3. python-pptx
   - **Purpose**: To create PowerPoint presentations programmatically.
   - **Usage**: This library is used to generate the actual PowerPoint presentation with slides, headers, and content.

## How the System Works

1. **API Key Setup**: The OpenAI API key is set using the `openai.api_key` parameter.

2. **User Input**: The system prompts the user to input the title of the presentation through the terminal.

3. **Prompt Generation**: The system defines a JSON structure for the OpenAI request, which includes placeholders for the presentation title and slide content. A question prompt is created, specifying the desired presentation format.

4. **OpenAI Interaction**: The system uses the OpenAI ChatCompletion API (model: gpt-3.5-turbo) to generate the presentation content based on the user's prompt. The API responds with a JSON structure containing slide data.

5. **Parsing JSON Response**: The JSON response from the API is parsed using the `json` library to extract the slide data.

6. **Presentation Creation**: The `python-pptx` library is used to create a PowerPoint presentation. For each slide in the extracted slide data, a new slide is added to the presentation. If a slide has a header, it is added as the title of the slide. If a slide has content, it is added to the slide's body.

7. **Saving the Presentation**: The final PowerPoint presentation is saved as 'output.pptx' in the current directory.

## How to Use

1. Run the script in your terminal.

2. Enter the desired title for your presentation when prompted.

3. The system will generate a presentation with 10 slides, each containing a header and informative content based on your chosen topic.

4. The final presentation will be saved as 'output.pptx' in the same directory.

Note: Ensure you have the required libraries (`openai` and `python-pptx`) installed before running the script. You can install `python-pptx` using 'pip install python-pptx'.
