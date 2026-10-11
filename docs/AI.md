# AI-assisted reading

[← Back to Ebok](../README.md) · [Download Alpha](../README.md#download)

Ebok helps you understand unfamiliar words without leaving the page. Its optional AI takes a selected word and a short excerpt around it, then generates a brief explanation in simple English for that context.

## Built with Llama

The public alpha uses **Meta’s Llama 3.2 1B Instruct**, with 4-bit weights, running locally through **WebLLM and WebGPU**.

| Component | Used in the alpha |
| :--- | :--- |
| Model | [Meta Llama 3.2 1B Instruct](https://huggingface.co/meta-llama/Llama-3.2-1B-Instruct) |
| Model package | [MLC’s Llama-3.2-1B-Instruct-q4f16_1-MLC](https://huggingface.co/mlc-ai/Llama-3.2-1B-Instruct-q4f16_1-MLC/tree/2a37b0a5ecb622d51ddc2fac74de0b95872affd7) |
| Runtime | [WebLLM](https://webllm.mlc.ai/) 0.2.85, accelerated by WebGPU |
| Processing | On your device, in a dedicated worker |
| First download | Approximately 700 MB; model files are cached locally |

![The Alice sample open in Ebok, with a completed on-device AI explanation for remarkable](../assets/ai-reading.png)

*Captured from the Alpha app after Llama generated the explanation on the device.* [View the AI popup up close](../assets/ai-explanation.png).

## Try the AI

1. Open a text-based book, such as the [Alice sample](../samples/README.md).
2. Select a single word and choose **Define**.
3. Choose **Enable AI · download ~700 MB** in the word popup.
4. Keep an internet connection while the model downloads. Dictionary meanings remain available while AI loads.
5. Once AI is ready, read the explanation beside the dictionary definition. Select another word and choose **Define** to use it again.

Your choice to enable AI is remembered. In later reading sessions, Ebok prepares the model in the background. Selecting text alone does not start an explanation; choosing **Define** does.

Choose **Turn off** in the AI panel to stop the model and release its GPU memory. Closing the reader also releases the model. Turning AI off retains downloaded files so they can be reused later.

## What stays on your device

The selected word and its passage are used for **local inference**. Ebok does not send that text to a hosted AI inference service, and the AI feature does not require an API key or an AI-service subscription.

The initial model and tokenizer files are downloaded from Hugging Face, and the compiled model library comes from MLC’s GitHub repository. After these files are cached, AI explanations can work offline. If the cache is cleared or evicted, the files need to be downloaded again.

Online dictionary fallback and translation are separate features that make requests to external services. A fallback lookup sends the queried word; translation sends the selected text. Ordinary reading and covered words in the bundled dictionary work offline.

## Requirements and limits

- A GPU and driver that support **WebGPU with `shader-f16`**. Availability and speed vary by device; desktop installer availability does not guarantee AI hardware support.
- Internet for the initial download, plus enough local storage for the cached model and available GPU memory to run it.
- In the browser version, a secure context such as HTTPS or localhost. The desktop app uses its own secure application origin.
- The alpha’s AI explains **one selected word in English using a short surrounding excerpt**. It can misinterpret a passage or decline when there is insufficient context. Dictionary definitions are shown separately.

If the model cannot load or loses access to the GPU, use **Retry AI**. For an incomplete or uncertain answer, choose **Try again** or continue with the dictionary. The reader remains usable without AI.

For an AI problem, [report a bug](https://github.com/xikiu/ebok-releases/issues/new?template=bug_report.yml) with the Ebok version, operating system, GPU if known, exact message, and a short example you can share.

## Model and runtime credits

Built with Llama. The model is developed by Meta; its weights are governed by the [Llama 3.2 Community License](https://github.com/meta-llama/llama-models/blob/main/models/llama3_2/LICENSE) and [acceptable use policy](https://www.llama.com/llama3_2/use-policy). The MLC model package is downloaded separately from the installer. [WebLLM](https://github.com/mlc-ai/web-llm) is provided by MLC under Apache-2.0.
