# MIMO TTS Multi-Voice Demo

Multi-voice speech synthesis demo using Xiaomi MiMo-V2.5-TTS API and Bitwarden Secrets Manager, orchestrated via GitHub Actions.

## Voices

| Voice | Language | Style |
|-------|----------|-------|
| 茉莉 (Moli) | Chinese | Female, standard |
| 冰糖 (Bingtang) | Chinese | Female, sweet |
| 苏打 (Soda) | Chinese | Female, crisp |
| 白桦 (Baihua) | Chinese | Male, deep |
| Mia | English | Female, friendly |
| Chloe | English | Female, warm |
| Milo | English | Male, energetic |
| Dean | English | Male, professional |

## How It Works

1. GitHub Actions workflow triggered on push or manually
2. [bws](https://github.com/bitwarden/sdk-sm) injects `MIMO_API_KEY` from Bitwarden Secrets Manager
3. Each voice is generated in parallel via strategy matrix
4. Audio saved as WAV files and published as build artifacts

## Run

Trigger the workflow manually:
```
gh workflow run "MIMO TTS Multi-Voice Demo"
```

Download artifacts from the Actions tab after completion.
