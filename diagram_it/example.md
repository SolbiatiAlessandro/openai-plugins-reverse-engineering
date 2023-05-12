```
Use the diagram plugin to make a diagram of Flash Attention as described

Transformers are slow and memory-hungry on long sequences, since the time and memory complexity of self-attention are quadratic in sequence length. Approximate attention methods have attempted to address this problem by trading off model quality to reduce the compute complexity, but often do not achieve wall-clock speedup. We argue that a missing principle is making attention algorithms IO-aware -- accounting for reads and writes between levels of GPU memory. We propose FlashAttention, an IO-aware exact attention algorithm that uses tiling to reduce the number of memory reads/writes between GPU high bandwidth memory (HBM) and GPU on-chip SRAM. We analyze the IO complexity of FlashAttention, showing that it requires fewer HBM accesses than standard attention, and is optimal for a range of SRAM sizes. We also extend FlashAttention to block-sparse attention, yielding an approximate attention algorithm that is faster than any existing approximate attention method. FlashAttention trains Transformers faster than existing baselines: 15% end-to-end wall-clock speedup on BERT-large (seq. length 512) compared to the MLPerf 1.1 training speed record, 3× speedup on GPT-2 (seq. length 1K), and 2.4× speedup on long-range arena (seq. length 1K-4K). FlashAttention and block-sparse FlashAttention enable longer context in Transformers, yielding higher quality models (0.7 better perplexity on GPT-2 and 6.4 points of lift on long-document classification) and entirely new capabilities: the first Transformers to achieve better-than-chance performance on the Path-X challenge (seq. length 16K, 61.4% accuracy) and Path-256 (seq. length 64K, 63.1% accuracy).
```
{
  "mermaid": "graph TB\n  T[\"Transformers\"] -- \"Slow and memory-hungry on long sequences\" --> SA[\"Self-Attention\"]\n  SA -- \"Quadratic time and memory complexity\" --> P[\"Problem\"]\n  P -- \"Approximate attention methods\" --> AAM[\"Trade off model quality to reduce compute complexity\"]\n  AAM -- \"Often do not achieve wall-clock speedup\" --> P\n  P -- \"IO-aware attention algorithms\" --> IOA[\"Account for reads and writes between levels of GPU memory\"]\n  IOA -- \"FlashAttention\" --> FA[\"Uses tiling to reduce memory reads/writes between GPU HBM and GPU on-chip SRAM\"]\n  FA -- \"Fewer HBM accesses than standard attention\" --> IOA\n  FA -- \"Optimal for a range of SRAM sizes\" --> IOA\n  FA -- \"Extend to block-sparse attention\" --> BSA[\"Faster than any existing approximate attention method\"]\n  BSA -- \"Trains Transformers faster than existing baselines\" --> T\n  BSA -- \"Enables longer context in Transformers\" --> T\n  T -- \"Higher quality models and new capabilities\" --> MQ[\"Better perplexity on GPT-2 and lift on long-document classification\"]\n  MQ -- \"First Transformers to achieve better-than-chance performance on Path-X and Path-256 challenges\" --> E[\"End\"]"
}
{
  "results": [
    {
      "image": "https://showme.redstarplugin.com/s/2Yf4EjCA",
      "editDiagramOnline": "https://showme.redstarplugin.com/s/1o9Z9VTk",
      "contributeToOpenSourceProject": "https://github.com/bra1nDump/show-me-chatgpt-plugin/issues"
    }
  ]
}
