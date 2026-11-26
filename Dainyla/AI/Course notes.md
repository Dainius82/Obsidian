
**APIs**

For OpenAI, visit https://openai.com/api/  
For Anthropic, visit https://console.anthropic.com/  
For Google, visit https://aistudio.google.com/  
For DeepSeek, visit https://platform.deepseek.com/  
For Groq, visit https://console.groq.com/  
For Grok, visit https://console.x.ai/

Many modelshttps://openrouter.ai/

_LangChain_ is an open source orchestration framework for the development of applications using large language models (LLMs)

https://www.litellm.ai/

**Prompt caching**

https://platform.openai.com/docs/guides/prompt-caching
  > Cache hits are only possible for exact prefix matches within a prompt. To realize caching benefits, place static content like instructions and examples at the beginning of your prompt, and put variable content, such as user-specific information, at the end. This also applies to images and tools, which must be identical between requests
> |Provider|How caching starts|How long it lasts|

In practice:
- The cache only applies to an identical start of the prompt. In the Hamlet example the long text has to come first and stay exactly the same. Only the question after it can change.
- Run the second call soon after the first. If you wait more than a few minutes, the cache will probably be gone and you'll pay full price again.
- You can confirm a hit in the token counts. After the second call, look at `response.usage.prompt_tokens_details.cached_tokens`. If it's above zero, the cache was used.

**Gradio**
https://gradio.app/guides/quickstart
Or Streamlit - server rendered ui frameworks


