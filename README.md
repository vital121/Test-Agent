# Test-Agent: Your intelligent test assistant
<p align="center">
  <img src="https://github.com/codefuse-ai/MFTCoder/blob/main/assets/github-codefuse-logo-update.jpg" width="50%" />
</p>

<p align="center">
    <a href="https://github.com/codefuse-ai/Test-Agent">
        <img alt="stars" src="https://img.shields.io/github/stars/codefuse-ai/Test-Agent?style=social" />
    </a>
    <a href="https://github.com/codefuse-ai/Test-Agent">
        <img alt="forks" src="https://img.shields.io/github/forks/codefuse-ai/Test-Agent?style=social" />
    </a>
    <a href="https://github.com/codefuse-ai/Test-Agent/LICENCE">
      <img alt="License: MIT" src="https://badgen.net/badge/license/apache2.0/blue" />
    </a>
    <a href="https://github.com/codefuse-ai/Test-Agent/issues">
      <img alt="Open Issues" src="https://img.shields.io/github/issues-raw/codefuse-ai/Test-Agent" />
    </a>
</p>

### Local Mac M1 experience effect
![Image](https://github.com/codefuse-ai/Test-Agent/assets/103973989/8dba860f-c1bb-49d5-b9dd-a58e541562a6)

### Magic Build Experience Effect
ModelScope TestGPT-7B: https://modelscope.cn/models/codefuse-ai/TestGPT-7B/summary
![MS](https://github.com/codefuse-ai/Test-Agent/assets/103973989/0e50b258-44f9-4dc6-8e30-0a01cf62d02b)


## What is Test Agent? （Introduction）

**Test Agent** aims to build an "intelligent entity" in the testing field, integrating large models and engineering technologies in the quality field to promote the upgrading of quality technology generations. We hope to work with community members to create innovative testing solutions and build a 24-hour online testing assistant service to make testing as smooth as silk.
## Features

* **Model** In this issue, we open-sourced the test domain model TestGPT-7B. The model is based on CodeLlama-7B and fine-tuned for related downstream tasks:
  * **Multi-language test case generation (Java/Python/Javascript)** has always been an area of ​​great concern in academia and industry. In recent years, new products or tools have been continuously incubated, such as EvoSuite, Randoop, SmartUnit, etc. However, traditional test case generation has its own pain points that are difficult to solve. Test case generation based on large models is superior to traditional test case generation tools in terms of test case readability, test scenario completeness, and multi-language support. This time, we focus on supporting multi-language test case generation. In our open source version, we first include the test case generation capabilities of Java, Python, and Javascript, and will gradually open up languages ​​such as Go and C++ in the next version.
  * **Test Case Assert Completion** When analyzing and exploring the current status of test cases, we found that a certain proportion of the stock test cases in the code repository do not contain Assert. Although test cases without Assert can be executed and passed during the regression process, they cannot find problems. Therefore, we have expanded the scenario of automatic completion of test case Assert. Through this model capability, combined with certain engineering support, batch automatic completion of test cases in the entire library can be achieved, intelligently improving the quality level of the project.

* **Engineering Framework** Local model rapid release and experience engineering framework
  - ChatBot Page
  - Model Quick Start
  - Private deployment, localized GPT large model interacts with your data and environment, no data leakage risk, 100% secure

**We will continue to iterate our models and engineering capabilities in the future:**
- Continue to add more exciting test domain application scenarios, such as domain knowledge quiz, test scenario analysis, etc.
- Support the opening of the copilot engineering framework for testing scenarios, such as intelligent embedding of test domain knowledge, general test tool API system, intelligent test agent, etc. Stay tuned!
- Based on 7B, it will be gradually expanded to 13B and 34B models. Welcome to follow!

## The most powerful 7B test field model (Model)
Currently in TestAgent, we use the TestGPT-7B model by default. Compared with the existing open source models, the TestGPT-7B model is at the industry leading level in terms of use case execution pass rate (pass@1) and use case scenario coverage (average number of test scenarios).
The evaluation results of the core capabilities of the TestGPT-7B model are as follows:
- Multi-language test case generation
For the three languages ​​supported by the model: Java, Python, and Javascript, the Pass@1 evaluation results are as follows:

| Model | Java pass@1 | Java Average number of test scenarios | Python pass@1 | Python Average number of test scenarios | Javascript pass@1 | Javascript Average number of test scenarios |
| --- | --- | --- | --- | --- | --- | --- |
| TestGPT-7B | 48.6% | 4.37 | 35.67% | 3.56 | 36% | 2.76 |
| CodeLlama-13B-Instruct | 40.54% | 1.08 | 30.57% | 1.65 | 31.7% | 3.13 |
| Qwen-14B-Chat | 10.81% | 2.78 | 15.9% | 1.32 | 9.15% | 4.22 |
| Baichuan2-13B-Chat | 13.5% | 2.24 | 12.7% | 2.12 | 6.1% | 3.31 |


- Test case Assert completion
The current model supports Assert completion for Java use cases. The Pass@1 evaluation results are as follows:

| Model | pass@1 | Percentage of strong validation |
| --- | --- | --- |
| Codefuse-TestGPT-7B | 71.1% | 100% |


## Engineering Architecture
![JG](https://github.com/codefuse-ai/Test-Agent/assets/103973989/1b61beff-df59-4ab3-843c-266413c8dbc4)

The clarion call for big models has been sounded, and big models in the testing field are also constantly evolving. Through the rich world knowledge accumulated during the pre-training process, they have demonstrated extraordinary reasoning and decision-making capabilities in complex interactive environments.

Although the basic model has achieved remarkable results in the testing field, there are still some limitations, and domain-specific testing tasks usually require specialized tools or domain knowledge to solve. For example, the basic model can complete tasks such as single test code generation and test text generation through pre-training knowledge, but when dealing with complex integrated use case generation, domain-specific use case generation, and test process pipeline interaction, more professional tools and fields are needed. Knowledge. Therefore, integrating specialized tools with basic models can give full play to their respective advantages. Specialized tools can solve the problem of insufficient model timeliness, enhance professional knowledge, improve interpretability and robustness. The basic model has human-like reasoning and planning capabilities, can understand complex data and scenarios, and interact with the real world.

Based on the open model engineering deployment and ChatBot in this issue, we will continue to invest deeply in the field of open source testing. Together with like-minded developers in the community, we will create the most advanced Tools engineering system, intelligent testing assistant and open source testing project in the testing field!

## Quick Start
### Prerequisites

#### Model Download

You can get detailed information about the model and download the model file on [modelscope](https://modelscope.cn/models/codefuse-ai/TestGPT-7B) or [huggingface](https://huggingface.co/codefuse-ai/TestGPT-7B).
have to be aware of is:
1) If you download the model through modelscope, please refer to [Download Instructions](https://www.modelscope.cn/docs/%E6%A8%A1%E5%9E%8B%E7%9A%84%E4%B8%8B%E8%BD%BD#%E4%BD%BF%E7%94%A8Git%E4%B8%8B%E8%BD%BD%E6%A8%A1%E5%9E%8B);
2) If you download the model via huggingface, please make sure you can access huggingface normally.

#### Environment Installation

- python>=3.8
- transformers==4.33.2

```plain
git clone https://github.com/codefuse-ai/Test-Agent
cd Test-Agent
pip install -r requirements.txt
```

Before you start running the TestGPT-7B model, make sure your execution environment has about 14GB of video memory.
### Start the service

The project provides the ability to quickly build a UI on the web page to more intuitively display model interactions and effects. We can use a few simple commands to wake up the front-end page and call the model capabilities in real time. In the project directory, start the following services in sequence:

1. **Start the controller**
![controller](https://github.com/codefuse-ai/Test-Agent/assets/103973989/e68ce187-c9f1-4ce8-9d59-ff9d8348d0ac)
python3 -m chat.server.controller

2. **Start the model worker**
![work](https://github.com/codefuse-ai/Test-Agent/assets/103973989/073e4e79-4005-4c98-87f7-0eaa0b2b1e22)
python3 -m chat.server.model_worker --model-path models/TestGPT-7B --device mps

(models/TestGPT-7B is the actual model file path)

For the startup mode, you can select the following configuration options as needed:
- --device mps Option to enable GPU acceleration on Mac computers (Apple Silicon or AMD GPUs);
- --device xpu option to enable acceleration on Intel XPU (Intel Data Center and Arc A-Series GPUs);
  - 需安装[Intel Extension for PyTorch](https://intel.github.io/intel-extension-for-pytorch/xpu/latest/tutorials/installation.html)
  - Set OneAPI environment variables: source /opt/intel/oneapi/setvars.sh
- --device npu is an option to enable acceleration on Huawei AI processors;
  - Need to install [Ascend PyTorch Adapter](https://github.com/Ascend/pytorch)
  - Set CANN environment variables: source /usr/local/Ascend/ascend-toolkit/set_env.sh
- --device cpu option to run using CPU alone, without GPU;
- --num-gpus 2 Option to specify concurrent GPUs to run.

3. **Start the web service**
python3 -m chat.server.gradio_testgpt
![web](https://github.com/codefuse-ai/Test-Agent/assets/103973989/340dae35-573b-4046-a3e8-e87a91453601)
After the service is ready, we can open the local web service address http://0.0.0.0:7860 and see the complete front-end page. There are two examples of [Single Test Generation] and [Assert Completion] at the bottom of the page. Clicking the button will automatically generate a sample text into the input box. Clicking the Send button will trigger the model to run. After waiting for a while (the running time depends on the performance of the local machine), you can see the complete answer.
![demo](https://github.com/codefuse-ai/Test-Agent/assets/103973989/fd24274c-729b-4ce7-8763-a083b39300fb)

## 🤗 Acknowledgements
This project is built on [FastChat](https://github.com/lm-sys/FastChat), and we would like to express our deep gratitude for their open source contributions!

## contact us
![testagent_wechat_3](https://github.com/codefuse-ai/Test-Agent/assets/106229399/dd803960-8952-4fbb-90b2-877ff792d2e3)






