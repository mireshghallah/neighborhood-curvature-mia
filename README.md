# Membership Inference Attacks against Language Models via Neighbourhood Comparison

This is the repository for the ACL 2023 paper: [Membership Inference Attacks against Language Models via Neighbourhood Comparison]([https://link-url-here.org](https://arxiv.org/pdf/2305.18462)https://arxiv.org/pdf/2305.18462)

If you want to run the experiments from **the paper** which involve **fine-tuned GPT-2 models**, use  [this repo](https://github.com/justusmattern27/neighbour-mia/tree/main).


If you want to use our attack on **pre-trained models**, and compare to the **likelihood ratio attack and other baselines**, you can use code here. Run the following command to run the membership inference attack, including the baselines, on a GPT-Neo model,using Pile as member and Xsum as non-members.

```
python run_mia_unified.py --output_name unified_mia --base_model_name EleutherAI/gpt-neo-2.7B --mask_filling_model_name t5-3b --n_perturbation_list 25 --n_samples 2000 --pct_words_masked 0.3 --span_length 2 --cache_dir cache --dataset_member the_pile --dataset_member_key text --dataset_nonmember xsum --ref_model gpt2-xl  --baselines_only --max_length 2000
```

This code borrows from [this repo](https://github.com/justusmattern27/neighbour-mia/tree/main).

# Citation
@inproceedings{mattern-etal-2023-membership,
    title = "Membership Inference Attacks against Language Models via Neighbourhood Comparison",
    author = "Mattern, Justus  and
      Mireshghallah, Fatemehsadat  and
      Jin, Zhijing  and
      Schoelkopf, Bernhard  and
      Sachan, Mrinmaya  and
      Berg-Kirkpatrick, Taylor",
    booktitle = "Findings of the Association for Computational Linguistics: ACL 2023",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.findings-acl.719",
    pages = "11330--11343",
    
}
