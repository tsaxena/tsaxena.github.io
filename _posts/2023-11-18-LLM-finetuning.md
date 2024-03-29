## LLM finetuning
I currently work on prompt engineering as a part of the firefly team. As a part of that work I have come accross a number of ways to finetune LLMs for usecases. I am going to summarize some of common techniques for finetuning LLMs.


# What are LLMs? 
Large language models (LLMs) are typically expansive deep neural networks, commonly used for tasks like language translation, text summarization, and notably, conversational AI. Studies have shown that transformer-based models, when trained on extensive datasets, exhibit strong proficiency in tackling natural language processing (NLP) tasks. Increasing the model's parameters appears to enhance its capabilities. To investigate the limits of this scalability, researchers observed that pushing the number of parameters beyond a certain threshold not only amplifies the model's capacity but also unveils context-learning abilities that are absent in smaller language models like BERT.

LLMs have the same model architecture (transformer based) and trained on similar pre-training tasks as smaller language models but are siginificantly scaled on model size, data and traiing compute.

LLMs are trained using unsupervised learning/ With unsupervised learning, models can find previously unknown patterns. Due to the extensive training, LLMs can generate text for a variety of tasks in zero-shot manner. Despite that, there are cases where we want to control the output of LLMs. There are 3 ways of customizing LLMs for specific tasks:
- Prompting: In-context learning, prepending instructions or providing examples to pre-trained LLM. Prompt is engineered and optimized to obtain desired output from LLM. Weights of the LLM are not modified.
   - Hard prompts like templates
   - 

- Fine-tuning: All parameters are updated in full fine-tuning but LLMs are hard to fine-tune and experiments can lead to catistrophic forgetting. A more efficient way of fine-tuning is parameter efficient fine-tuning where only a small fraction of model parameters are updated while other parameters are frozen. Adapter-tuningm inserts additional task-specific layers between the
layers of pre-trained LLMs and only tunes parameters in the adapters. [PEFT](https://huggingface.co/docs/peft/index) is a library for efficiently adapting pre-trained language models (PLMs) to various downstream applications without fine-tuning all the model’s parameters.
   - Prompt Tuning
   - Prefix Tuning
   - P-Tuning
   - LoRA
   - Prompt Tuning	
   - IA3



# References
- [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223)
- [Nvidia Blog: LLMs](https://www.nvidia.com/en-us/glossary/data-science/large-language-models/)
- [Cohere LLM University](https://docs.cohere.com/docs/intro-large-language-models)
- [Parameter Efficient Transfer Learning](https://arxiv.org/abs/1902.00751)
- [Andriej Karpathy: Intro to LLM](https://www.youtube.com/watch?v=zjkBMFhNj_g)



<!-- Due to a plugin called `jekyll-titles-from-headings` which is supported by GitHub Pages by default. The above header (in the markdown file) will be automatically used as the pages title.

If the file does not start with a header, then the post title will be derived from the filename.

This is a sample blog post. You can talk about all sorts of fun things here.

---

### This is a header

#### Some T-SQL Code

```tsql
SELECT This, [Is], A, Code, Block -- Using SSMS style syntax highlighting
    , REVERSE('abc')
FROM dbo.SomeTable s
    CROSS JOIN dbo.OtherTable o;
```

#### Some PowerShell Code

```powershell
Write-Host "This is a powershell Code block";

# There are many other languages you can use, but the style has to be loaded first

ForEach ($thing in $things) {
    Write-Output "It highlights it using the GitHub style"
}
``` -->

    
