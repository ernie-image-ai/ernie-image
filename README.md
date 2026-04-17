# ERNIE-Image

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![LongTextBench](https://img.shields.io/badge/LongTextBench-0.9733-brightgreen)
![GENEval](https://img.shields.io/badge/GENEval-0.8856-brightgreen)
![Model](https://img.shields.io/badge/model-8B-orange)

ERNIE-Image is Baidu's open-source image generation model, excelling at **accurate text rendering in both Chinese and English**, structured layout generation, and photorealistic outputs. It achieves state-of-the-art scores on LongTextBench (0.9733) and GENEval (0.8856).

---

## Why ERNIE-Image?

| Feature | ERNIE-Image | FLUX.1 | Midjourney | Stable Diffusion |
|---|---|---|---|---|
| Chinese text rendering | ✅ Excellent | ❌ Poor | ❌ Poor | ❌ Poor |
| Bilingual (CN + EN) | ✅ Native | ❌ | ❌ | ❌ |
| Structured layout | ✅ Strong | ⚠️ Limited | ⚠️ Limited | ⚠️ Limited |
| Open source | ✅ Apache 2.0 | ✅ | ❌ | ✅ |
| Commercial use | ✅ Free | ⚠️ Dev only | ❌ | ✅ |

---

## Key Features

- **Accurate text rendering** — generates readable Chinese and English text inside images, including posters, book covers, and UI mockups
- **Bilingual layouts** — natively handles mixed Chinese/English in a single composition
- **Structured design** — produces magazine spreads, infographics, comic panels, and product cards with clean visual hierarchy
- **8B open model** — Apache 2.0 licensed, free for commercial use
- **Turbo & Standard modes** — fast generation or higher quality, your choice

---

## Sample Outputs

**Text rendering — webpage mockup**
![Webpage mockup](https://cdn.ernie-image.com/showcase/ep/text_web.webp)

**Bilingual poster — tea ceremony**
![Bilingual tea poster](https://cdn.ernie-image.com/showcase/features/bilingual_tea.webp)

**Structured layout — manga comic**
![Manga comic layout](https://cdn.ernie-image.com/showcase/features/layout_comic.webp)

**Commercial use — skincare product**
![Skincare product shot](https://cdn.ernie-image.com/showcase/features/commercial_skincare.webp)

---

## Try It Online

**[ernie-image.com](https://ernie-image.com)** — no setup required, free credits on sign-up.

- **Turbo mode**: fast generation, ideal for iteration
- **Standard mode**: highest quality, best for final outputs
- Supports long text prompts, bilingual content, and complex layouts

---

## API Usage (via fal.ai)

```bash
# Submit a generation job
curl -X POST https://queue.fal.run/fal-ai/ernie-image/turbo \
  -H "Authorization: Key $FAL_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "prompt": "A luxury skincare product poster with Chinese and English text, clean white background, professional photography style",
    "image_size": "landscape_4_3"
  }'

# Poll for result
curl https://queue.fal.run/fal-ai/ernie-image/requests/{request_id}/status \
  -H "Authorization: Key $FAL_KEY"
```

Get your API key at [fal.ai](https://fal.ai).

---

## Prompt Tips

**For text rendering:**
> Include the exact text you want in quotes within the prompt. Be explicit about font style, placement, and language.

**For bilingual content:**
> Specify both languages explicitly, e.g., "with Chinese headline and English subtitle"

**For comic/manga layouts:**
> Describe the panel structure: "4-panel manga layout, black borders, action scene top-left, dialogue bottom-right"

**For product photography:**
> Add lighting and background details: "studio lighting, pure white background, shadow underneath"

---

## Resources

- [ernie-image.com](https://ernie-image.com) — web app
- [Hugging Face](https://huggingface.co/THUDM/CogView4-6B) — model weights
- [fal.ai/models/fal-ai/ernie-image](https://fal.ai/models/fal-ai/ernie-image) — API
- [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0)
