# Desafio: Integração com Azure OpenAI e Semantic Kernel

## Resumo

Este projeto explora o uso do Azure OpenAI e sua integração com o Semantic Kernel para desenvolver aplicações práticas. O Azure OpenAI permite a utilização de modelos de linguagem avançados, enquanto o Semantic Kernel fornece um conjunto de ferramentas que facilita a criação de aplicações cognitivas.

## Objetivos do Projeto

- Compreender as funcionalidades do Azure OpenAI.
- Realizar chamadas de API REST para gerar textos.
- Integrar o Semantic Kernel para aprimorar o fluxo de processamento de dados.

## Conteúdo Aprendido

1. **Azure OpenAI**:
   - Configuração do serviço no portal Azure.
   - Como autenticar e realizar chamadas de API para gerar respostas de texto.

2. **Semantic Kernel**:
   - Introdução ao Semantic Kernel e suas funcionalidades.
   - Exemplos de como integrar o Semantic Kernel com o Azure OpenAI para criar aplicações que entendem e geram linguagem natural.

## Implementação

A implementação consiste em uma série de chamadas de API que demonstram a geração de texto usando o Azure OpenAI. Abaixo estão alguns exemplos de código:

### Exemplo de Chamada de API

```python
import requests

# Configurações da API
api_url = "https://<sua-regiao>.api.azure.com/openai/deployments/<seu-modelo>/completions?api-version=2022-12-01"
headers = {
    "Content-Type": "application/json",
    "api-key": "<sua-chave>"
}
data = {
    "prompt": "Como funciona a integração do Azure OpenAI com o Semantic Kernel?",
    "max_tokens": 100
}

response = requests.post(api_url, headers=headers, json=data)
print(response.json())
```

## Integração com o Semantic Kernel

# Exemplo básico de integração com Semantic Kernel
```from semantic_kernel import Kernel```

# Inicialização do Kernel
```kernel = Kernel()```

# Adicionando um serviço de linguagem
```kernel.add_service("openai", "my_openai_service")```

# Executando uma função
```
result = kernel.run("openai", "generate_text", "Explique o Semantic Kernel.")
print(result)
```
## Conclusão

Este projeto demonstrou como o Azure OpenAI e o Semantic Kernel podem ser usados juntos para criar aplicações que compreendem e geram texto de maneira eficaz. A integração entre esses serviços permite o desenvolvimento de soluções mais inteligentes e responsivas.

Links Úteis

[Documentação do Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/reference)

[Introdução ao Semantic Kernel](https://learn.microsoft.com/en-us/semantic-kernel/overview/)

[Slides de Aplicação de Chats e Configurações API](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fhermes.dio.me%2Ffiles%2Fassets%2F691028e1-c693-48ad-b995-fdb42a184b68.pptx&wdOrigin=BROWSELINK)
