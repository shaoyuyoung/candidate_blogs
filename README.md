# 🗂️candidate_blogs
> [!NOTE]
> 
> This repo is temporary and used to record some notes (as blogs). All the blogs will be merged into my [homepage](https://shaoyuyoung.github.io/) in my spare time.

## 🛠️AI Infra
#### How to debug a PyTorch model?
outline@shaoyu: It is widely accepted that a DL model is essentially a piece of code (for pytorch, it is a python class inherits from `torch.nn.Module`). Sometimes, we may encounter some errors when running the code. Of course, it may be a potential bug in pytorch, but the majority of the time, it is a buggy code itself, we should repair the code to let it be executed normally. Here are some tips for us to debug pytorch code.

#### How should we submit a bug report for PyTorch?
outline@shaoyu: After you debug a pytorch model, you are sure that your code is correct but it still throws an error. Congratulations! You may find a potential bug in pytroch. The next step is to clean up the code and report it to the pytorch community. It's **very very very important for us to draft a nice bug report**. I'll cover this in more detail in this section.

#### How should we fix bugs based on bug reports for PyTorch?
outline@shaoyu: After submitting your bug report, maintainers will check your bug reports in their spare time. Sometimes, they may think your bug report is **high priority** and take action to fix the bug correctly. Well, to be honest, from my experience, most of the bugs are edge cases (because pytorch is a well-tested software system). Maintainers may not care these edge cases. However, Some edge cases are very easy to fix (e.g., adding a simple error checking). So maybe you can fix these edge cases by yourself (by submitting PRs), and then you will be one of the contributors of pyotrch (that's so cool!). I will introduce how we can fix some easy edge cases to contribute to pytorch.


@shaoyu: backup some instructions on modifying pytorch in developer mode.

First, you need to install pytorch from source, Here is the detailed instructions provided by offical document
https://github.com/pytorch/pytorch?tab=readme-ov-file#get-the-pytorch-source


this command group used to update pytorch (everytime you pull the remote code)
```
cd {YOUR_INTALLTION_DIR}/pytorch
git fetch origin
git checkout origin/{YOUR_BRANCH_NAME}

# update submudules
git submodule sync
git submodule update --init --recursive

# rebuild pytorch
python setup.py develop
```


## 🛡️Fuzz Testing

#### How to design a simple and effective fuzzing tool?
outline@shaoyu: To be honest, I'm not very familiar with C++ fuzzing (e.g., AFL, AFL++, OSS-fuzz). So this section aims to use these tools easily (I will also keep learning myself).

#### How to generate DL model to fuzz a DL system (library or compiler, such as PyTorch, ONNX, TVM)?
outline@shaoyu: After understanding the fundamentals of fuzzing, we move closer to our goal: fuzzing AI Infra! The basic element for this is a DL model. We have a formula: **`DL system fuzzing = Generating DL models`**. I will introduce how can we generate a DL model (valid and diverse), by using [NNSmith](https://github.com/ise-uiuc/nnsmith).


## 🤖Large Language Models

#### Some issues we may encounter when using vLLM or SGLang for LLM local deployments
outline@shaoyu: The goal of this section is to address some issues when we install and use LLM inference enginees. These engines are in highly rapid development and not stable, resulting in some easy instructions being needed.

#### Some considerations for invoking API services
outline@shaoyu: Well, invoking API services is usually costly. A few practical tips can prevent us from wasting unnecessary 🤑**money** in the initial debugging and large-scale experiments.

## 🤔What happens when they get together?
> [!IMPORTANT]
> 
> Actually, my research focuses on the intersection of the above three areas. So it is necessary to introduce **how we can use *LLM*-based *fuzzing* techniques to test *AI Infras***.
>

#### Prompt design
#### Test (Code) generation
#### Test Execution for Infra
#### Result Analysis
#### Feedback guidance
