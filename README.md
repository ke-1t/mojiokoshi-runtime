# mojiokoshi-runtime

Distribution point for the first-run model download of **MojiOkoshi**
(Studio Louis). This repository only hosts release assets; it contains
no product code.

## Release v1: Japanese punctuation model (int8)

- `model_int8.onnx` — an INT8 dynamically-quantized build of
  [japan-opendata/ja-punct-restore-v1](https://huggingface.co/japan-opendata/ja-punct-restore-v1)
  (Apache License 2.0), produced with ONNX Runtime quantization from
  the original ONNX weights. Quantization only shrinks the download;
  the model inserts 、/。/？/！ and never rewrites recognised words.
- `tokenizer.json` — the tokenizer file from the same repository
  (Apache License 2.0).

Base model: sbintuitions/modernbert-ja-130m (Apache License 2.0);
training data derived from HuggingFaceFW/fineweb-2 (ODC-By 1.0).

SHA-256:

- model_int8.onnx: `2be511f11eebada4bed8301242c4657e01820537af3e6106e08d201177be7229`
- tokenizer.json: `0dbdcf9ac15a56783bbd5781168332f7088cc9a1cf396c41419e72b87bfa57fc`
