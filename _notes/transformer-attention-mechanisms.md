---
title: "Transformer Attention Mechanisms"
date: 2024-03-20
tags: [transformers, attention, deep-learning]
---

Quick notes on different attention mechanisms in transformers and their trade-offs.

## Self-Attention vs Cross-Attention

**Self-Attention**: Query, Key, Value all come from the same sequence
- Used in encoder layers
- Helps model understand relationships within the input

**Cross-Attention**: Query from one sequence, Key/Value from another
- Used in decoder layers
- Connects encoder output to decoder

## Multi-Head Attention Benefits

```python
# Simplified multi-head attention
def multi_head_attention(Q, K, V, num_heads):
    head_outputs = []
    for i in range(num_heads):
        head_Q = linear_projection(Q, i)
        head_K = linear_projection(K, i)
        head_V = linear_projection(V, i)
        
        attention_output = scaled_dot_product_attention(head_Q, head_K, head_V)
        head_outputs.append(attention_output)
    
    return concatenate_and_project(head_outputs)
```

## Key Insights

- Multiple heads allow the model to attend to different types of relationships
- Each head can specialize in different aspects (syntax, semantics, etc.)
- Computational complexity is O(n²) with sequence length

## Optimization Ideas

- **Sparse Attention**: Only compute attention for local windows
- **Linear Attention**: Approximate attention with linear complexity
- **Flash Attention**: Memory-efficient attention computation 