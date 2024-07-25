# Config-Imports-TypeScript

Para ter uma experiência semelhante à das IDEs da JetBrains, onde há essas legendas contextuais, você pode usar uma combinação de extensões e configurações no Visual Studio Code. A extensão que mais se aproxima disso é a **IntelliSense** nativa do VS Code em combinação com o **TypeScript Hero**.

### Passos para configurar:

1. **TypeScript Hero**:
    - Abra o Visual Studio Code.
    - Vá para a barra lateral e clique em "Extensões" (ícone de quadrados).
    - Pesquise por "TypeScript Hero".
    - Clique em "Instalar".

2. **Habilitar IntelliSense**:
    - Abra o arquivo `settings.json` (você pode encontrar este arquivo nas configurações do VS Code).
    - Adicione as seguintes configurações para garantir que o IntelliSense esteja completamente habilitado e otimizado:

    ```json
    {
      "typescript.suggest.enabled": true,
      "typescript.suggest.completeFunctionCalls": true,
      "typescript.hero.imports.organizeOnSave": true,
      "typescript.hero.imports.stringQuoteStyle": "single"
    }
    ```

3. **Configurações adicionais**:
    - Certifique-se de que seu projeto está configurado corretamente para TypeScript e que você tem os tipos instalados. Isso pode ser feito garantindo que o `tsconfig.json` esteja configurado corretamente e que as dependências de tipos estejam instaladas.

### Exemplo do `tsconfig.json`:
    
```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true,
    "jsx": "react",
    "baseUrl": "./",
    "paths": {
      "@components/*": ["src/components/*"],
      "@utils/*": ["src/utils/*"]
    }
  }
}
```
<hr> 

Essas configurações fazem parte do arquivo `tsconfig.json`, que é usado para configurar o compilador TypeScript. Vou explicar o que cada uma delas significa:

1. **`target`**: Define a versão do ECMAScript (ES) para a qual o TypeScript deve compilar. Nesse caso, está definido como ES6.

2. **`module`**: Especifica o sistema de módulos a ser usado. "commonjs" é comum para ambientes Node.js.

3. **`strict`**: Quando ativado, o TypeScript aplica verificações rigorosas, como checagem de tipos mais estrita.

4. **`esModuleInterop`**: Permite interoperabilidade entre módulos ES6 e CommonJS.

5. **`skipLibCheck`**: Quando ativado, o TypeScript não verifica arquivos de definição de bibliotecas externas.

6. **`forceConsistentCasingInFileNames`**: Garante consistência nos nomes de arquivos (maiúsculas/minúsculas).

7. **`jsx`**: Define como o TypeScript deve tratar JSX (usado em React). Aqui, está configurado para "react".

8. **`baseUrl`**: Define o caminho base para os módulos. No seu caso, é o diretório raiz ("./").

9. **`paths`**: Mapeia caminhos de importação para diretórios específicos. Por exemplo, "@components/*" mapeia para "src/components/*".

Essas configurações ajudam a personalizar o comportamento do compilador TypeScript para o seu projeto. 😊

### Uso:
Depois de configurar essas extensões e ajustes, você verá melhorias significativas no autocompletar e dicas contextuais do Visual Studio Code. Embora possa não ser exatamente igual ao que as IDEs da JetBrains oferecem, deve proporcionar uma experiência bastante próxima.
