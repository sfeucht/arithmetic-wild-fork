# Rebuttal Results for Arithmetic in the Wild: Llama uses Base-10 Addition to Reason about Cyclic Concepts

Thank you for the great feedback!

See `neuron_rebuttal.pdf` for these results:
1. We’ve added ablations for 16 additional templates for which Llama has 70% accuracy or higher. Our results are robust: e.g., prompts having to do with scheduling a haircut in [offset] months show similar results to the templates we trained on. We emphasize that these interventions only affect 28 out of 14336 neurons in MLP 18 ($\frac{1}{16384}=$ 0.006% of MLP neurons at the last token position), and that ablating 28 random neurons has no effect across 10 seeds.
2. We share results for a sweep over neuron thresholds. By using a slightly more lenient threshold, we find six extra neurons, that when combined with our original 28 neurons, explain 100% of Llama’s performance for addition. These neurons appear to behave similarly to the ones we studied in-depth in the main text (based on activation patterns and alignment with Fourier probes). 

See `fourier_rebuttal.pdf` for extra Fourier steering results:
1. `{addition,hours,months,weekdays}_target_topk_after_steering.pdf` show top-1,2,3 accuracy for Fourier steering experiments with $\alpha=10$. 
2. `months_mean_prob_matrix_scale_grid.pdf` shows heatmaps for model output probabilities when steering Fourier probes for $T\in\{2,5,10,50\}$ with $\alpha\in\{1,5,10,15,20,25,30,35\}$. Even for smaller scaling factors, we can observe that probability mass shifts most towards the desired output concept. 
