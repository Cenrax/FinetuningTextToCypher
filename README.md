# FinetuningTextToCypher
This is a demo project where I have finetuned Llama3 8b model quantized in 4bit


I have Unsloth framework for finetuning the Llama3 8B model.

Total memory usage:
![image](https://github.com/Cenrax/FinetuningTextToCypher/assets/43017632/772e7cef-8bde-488d-943d-42201f565c5c)


```mermaid
graph TD
    A("1. Finetuning dataset preparation using gpt4 turbo") --> B("2. Run dataset on neo4j server to validate the generated queries; add 'is_success' field")
    B --> C("3. Load the Llama3 8b model from Hugging Face")
    C --> D("4. Add quantization in 4 bit")
    D --> E("5. Finetunedb using LORA for 1 epoch using Unsloth framework")
    E --> F("6. Saved the model locally")
```

Future steps:
-[X] Convert the model to gguf format
-[] Load the model in LMStudio
-[] Experimentation of loading the model in mobile device
-[] Ran it locally for Cypher generation

