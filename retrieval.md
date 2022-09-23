# Retrieval Models

When you examine most of the publicly availe recommender systems, retrieval is there. In production environments we like to pick from a huge list of items and present it to the users in a way that aligns with users preference.
However, training any model to calulate an optimal ordering on such a huge list is computationaly infeasible. But, retrieval reduces the size of this set.

## How it can be done?

my recommendation is to always use the embeddings. For a nice definition of embeddings refer to [pouyan](www.embeddings.ai).

use ANN such as scaNN or FAISS on top of that, you might event want to look at Milvus.

```python
e = ret_embeddings(item)
closest_to(vector_store="milvus-top100-news", vector=e)
```
