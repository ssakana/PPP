# LANG: A Lesson Plan Generation Framework via Multi-Form Interaction with Large Language Models

## Dataset

#### Quality analysis

Quality analysis of our Plan10k. "P" denotes primary school, "J" denotes junior high school, and "H" denotes high school.

<div style="text-align: center;">
  <img src="imgs/plan10k.png">
</div>

## Visualization
### Visualization of lesson plan.
Here are the lesson plan for the lesson on “Biodiversity”.
<div style="text-align: center;">
  <img src="imgs/plan en.png" width="49%" style="display: flex" height="732px">
  <img src="imgs/plan zh.png" width="49%" style="display: flex" height="732px">
</div>


#### Visualization of presentation generation.
Here are the slides for the lesson on “Biodiversity”.

<div style="text-align: center;">
  <img src="imgs/ppt en.png">
</div>
<div style="text-align: center;">
  <img src="imgs/ppt zh.png">
</div>


#### Visualization of podcast.
Here is an excerpt of podcast content for the lesson on “Biodiversity”, and the audio can be downloaded from here: [en](files/podcast%20en.wav?raw=True), [zh](files/podcast%20zh.wav?raw=True).

<div style="text-align: center;">
  <img src="imgs/podcast en.png">
</div>

<div style="text-align: center;">
  <img src="imgs/podcast zh.png">
</div>

### Access

Our dataset samples are available in the [dataset](dataset) directory. The samples are in JSON format and can be accessed as follows:

```python
import json
samples = json.load(open('dataset/en-samples-10.json', encoding='utf-8'))
```

### Dataset Details

Each data entry includes `id`, `language`, `query`, `input` and `output`. The `query` refers to the teacher's inquiry (knowledge point), the `input` is the prompt provided to the LLMs, and the `output` is a complete lesson plan.

```json
{
    "id": "01",
    "language": "en",
    "query": "...",
    "input": "...",
    "output": "..."
}
```

## Comparing

Comparison of chapter correction before and after based on GPT Score:

<div style="text-align: center;">
  <img src="imgs/comparing.png">
</div>

Teacher satisfaction:

<div style="text-align: center;">
  <img src="imgs/human score on en.png" width=49%>
  <img src="imgs/human score on zh.png" width=49%>
</div>

## Demo
The following is a complete set of lesson plan, presentation, and podcast.

||en|zh|
|:-----|:-----:|:-----:|
|plan|[view](files/plan%20en.pdf)|[view](files/plan%20zh.pdf)|
|presentation|[view](files/ppt%20en.pdf)|[view](files/ppt%20zh.pdf)|
|podcast|[download](files/podcast%20en.wav?raw=True)|[download](files/podcast%20zh.wav?raw=True)|
