# Tiny Shakespeare Model Comparison

Training an RWKV-inspired "Student" model vs GPT on character-level Shakespeare using [nanoGPT](https://github.com/karpathy/nanoGPT).

## Results (1000 iterations)

| Model | Parameters | Final Val Loss | Time/Iter |
|-------|-----------|----------------|-----------|
| Student (RWKV-style) | 0.83M | 1.38 | ~155ms |
| GPT | 10.65M | 1.32 | ~525ms |

The Student model is **13x smaller** and **3x faster** per iteration, with only slightly higher loss.

## Model Configs

**Student**: 5 layers, 128 embed dim, linear attention with exponential decay

**GPT**: 6 layers, 6 heads, 384 embed dim, standard transformer attention

## Usage

Run the notebook in Google Colab with GPU runtime.
