# R2 MC STUDIO PRO

Aplicativo Android de gravação e produção musical (WebView + assets do Estúdio R2).

**Nome do pacote:** `com.r2mc.studiopro`  
**Versão:** 1.0.0  
**Min SDK:** 24 (Android 7.0)  
**Target SDK:** 34

---

## Como gerar o APK (método recomendado – GitHub Actions)

Você **não precisa** de Android Studio nem de computador poderoso.

### Passo a passo (3–5 minutos)

1. Crie uma conta gratuita no [GitHub](https://github.com) (se ainda não tiver).

2. Crie um repositório **novo e vazio** (ex: `r2-mc-studio-pro`).  
   - Marque como **Public** (necessário para Actions gratuitas sem limite de minutos extras).  
   - **Não** adicione README, .gitignore ou license na criação.

3. No seu celular ou computador, faça o upload deste projeto:

   **Opção A – Pelo site do GitHub (mais fácil no celular):**
   - Entre no repositório → clique em **uploading an existing file**
   - Arraste **todos** os arquivos e pastas deste ZIP (incluindo a pasta `.github`)
   - Commit com a mensagem `Initial commit`

   **Opção B – Pelo Git (computador):**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - R2 MC Studio Pro"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/r2-mc-studio-pro.git
   git push -u origin main
   ```

4. Vá na aba **Actions** do repositório.

5. Clique no workflow **Build R2 MC Studio Pro APK** → **Run workflow** → **Run workflow**.

6. Aguarde 3–8 minutos. Quando aparecer o check verde, clique na execução.

7. Na seção **Artifacts**, baixe o arquivo **R2_MC_STUDIO_PRO-debug**.

8. Extraia o ZIP do artefato → você terá o `app-debug.apk`.

9. Transfira o APK para o celular e instale (pode precisar ativar “Instalar apps de fontes desconhecidas”).

---

## O que o APK faz (quando instalado)

- Solicita permissão de microfone corretamente
- Grava voz (MediaRecorder)
- Importa arquivos de áudio
- Reproduz faixas
- Visualizador de forma de onda
- Timer de gravação
- Lista de faixas com play / download / remover
- Funciona **offline**
- Interface em português brasileiro

---

## Limitações conhecidas desta versão

Esta é a versão **1.0** baseada em WebView.  
Ainda **não** possui:

- Editor multipista completo (timeline, corte, fade avançado)
- Efeitos DSP nativos (EQ, compressor, reverb, Auto-Tune)
- Exportação profissional WAV/MP3 com engine nativo
- Gravação em background com tela bloqueada robusta

Esses recursos exigem desenvolvimento nativo adicional (NDK/Oboe).

---

## Estrutura do projeto

```
R2_MC_STUDIO_PRO/
├── .github/workflows/build-apk.yml   ← workflow de compilação
├── app/
│   ├── build.gradle
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── assets/                   ← index.html, app.js, styles.css
│       ├── java/.../MainActivity.java
│       └── res/
├── build.gradle
├── settings.gradle
├── gradle.properties
├── gradlew
└── README.md
```

---

## Licença

Uso pessoal e educacional. Os assets de áudio e o código WebView são de domínio do projeto R2 MC.
