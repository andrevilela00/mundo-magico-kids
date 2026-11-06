# Vozes da Mundo Mágico Kids

A aplicação suporta clips MP3 pré-gravados por idioma, com fallback para a voz do Safari enquanto não existirem ficheiros.

## Formato

Guarda os MP3 em `audio/pt-PT/` e `audio/en-GB/`. Regista cada um no ficheiro `audio/manifest.json`:

```json
{
  "pt-PT": {"game-0-question":"audio/pt-PT/game-0-question.mp3"},
  "en-GB": {"game-0-question":"audio/en-GB/game-0-question.mp3"}
}
```

Para cada idioma, as chaves são `game-0-question` até `game-3-question`, `game-0-correct` até `game-3-correct`, `game-0-incorrect` até `game-3-incorrect`; equivalentes `story-0` até `story-2`; e `game-end`, `story-end`.

O texto exato de cada fala está definido no `index.html`. Gere as vozes com uma voz juvenil expressiva licenciada e com sotaque nativo pt-PT e en-GB, ouvindo e aprovando cada clip antes de publicar. Evita utilizar gravações de crianças reais sem consentimento e direitos adequados.

**Segurança:** nunca colocar chaves de API de fornecedores de áudio no JavaScript público ou no repositório. A geração de MP3 deve ser feita fora do site, numa ferramenta segura, e só os ficheiros finais devem ser publicados.

**Estado:** o manifesto começa vazio. Enquanto não forem adicionados MP3, a narração continua a usar a síntese de voz do navegador. O GitHub Pages é público.
