# Critical-Questions-of-Thought: Steering LLM reasoning with Argumentative Querying

Combining argumentation theories, leveraging Toulmin's argument schema and the notions of critical questions, with the test-time compute paradigm enables LLMs' higher performances on logical and mathematical tasks. In particular, the probing action of the critical questions allows the model to adjust its reasoning plan, thus effectively correcting itself in case of wrong assumptions or thinking steps. The ensuing approach, denoted as _Critical-Questions-of-Thought (CQoT)_, is composed of a pipeline rendered herein as a Python script.  

<br>

We share the results achieved by the CQoT method as detailed in our [paper](https://arxiv.org/abs/2412.15177).

<br>

The colour-coded evals [CQoT_Evals.xlsx](CQoT_Evals.xlsx) present the scores reached by 5 LLMs, both proprietary and open source, on 40 challenging questions retrieved from [MT-Bench Reasoning and Math benchmark](https://huggingface.co/datasets/HuggingFaceH4/mt_bench_prompts). Each model has been tested on its baseline, as well as CoT and CQoT implementation. Scores, assigned by an LLM judge (GPT-4o), span from 1 to 10 and reflect the performance of each model on the specific query. Low-graded responses (1-4) are displayed with a red background. Middle-ranged replies (5-7) are coloured in yellow, whereas good answers (8-10) are showcased in green.

<br>

Here we can preview the outcome of the experiments we accomplished to evaluate CQoT. 

<br>

<table>
  <tr>
    <th rowspan="2">Models + CQoT</th>
    <th colspan="2">MT-Bench (Reasoning)</th>
    <th colspan="2">MT-Bench (Math)</th>
  </tr>
  <tr>
    <th>Standard</th>
    <th>CoT</th>
    <th>Standard</th>
    <th>CoT</th>
  </tr>
  <tr>
    <td>Claude Sonnet 3.5</td>
    <td style="background-color:#c6efce;">+4.06%</td>
    <td style="background-color:#c6efce;">+4.68%</td>
    <td style="background-color:#c6efce;">+5.95%</td>
    <td style="background-color:#ffffcc;">+0%</td>
  </tr>
  <tr>
    <td>GPT-4.0</td>
    <td style="background-color:#c6efce;">+1.81%</td>
    <td style="background-color:#c6efce;">+3.04%</td>
    <td style="background-color:#c6efce;">+1.05%</td>
    <td style="background-color:#c6efce;">+7.26%</td>
  </tr>
  <tr>
    <td>Gemini 1.5-pro-001</td>
    <td style="background-color:#c6efce;">+5.33%</td>
    <td style="background-color:#c6efce;">+7.88%</td>
    <td style="background-color:#c6efce;">+10.29%</td>
    <td style="background-color:#c6efce;">+9.04%</td>
  </tr>
  <tr>
    <td>Llama 3.1-70b-Instruct</td>
    <td style="background-color:#c6efce;">+4.35%</td>
    <td style="background-color:#c6efce;">+1.12%</td>
    <td style="background-color:#c6efce;">+6.70%</td>
    <td style="background-color:#c6efce;">+2.14%</td>
  </tr>
  <tr>
    <td>Nemotron-51b-Instruct</td>
    <td style="background-color:#c6efce;">+8.15%</td>
    <td style="background-color:#ffcccc;">-5.19%</td>
    <td style="background-color:#c6efce;">+4.57%</td>
    <td style="background-color:#c6efce;">+7.02%</td>
  </tr>
  <tr>
    <td><b>Average</b></td>
    <td style="background-color:#d9e2f3;"><b>+4.74%</b></td>
    <td style="background-color:#d9e2f3;"><b>+4.48%</b></td>
    <td style="background-color:#d9e2f3;"><b>+5.71%</b></td>
    <td style="background-color:#d9e2f3;"><b>+5.09%</b></td>
  </tr>
</table>


<br>

If you find our paper or pipeline useful, please consider referencing it:
```
@misc{castagna2024criticalquestionsofthoughtsteeringllmreasoning,
      title={Critical-Questions-of-Thought: Steering LLM reasoning with Argumentative Querying}, 
      author={Federico Castagna and Isabel Sassoon and Simon Parsons},
      year={2024},
      eprint={2412.15177},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2412.15177}, 
}
