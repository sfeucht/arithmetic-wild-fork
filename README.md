# Rebuttal Results for Arithmetic in the Wild: Llama uses Base-10 Addition to Reason about Cyclic Concepts

See `rebuttal_results.pdf` for extra results for COLM reviewers. Thank you for the great feedback!

1. We’ve added ablations for 16 additional templates for which Llama has 70% accuracy or higher. Our results are robust: e.g., prompts having to do with scheduling a haircut in [offset] months show similar results to the templates we trained on. We emphasize that these interventions only affect 28 out of 14336 neurons in MLP 18 ($\frac{1}{16384}=$ 0.006% of MLP neurons at the last token position), and that ablating 28 random neurons has no effect across 10 seeds.
2. We share results for a sweep over neuron thresholds. By using a slightly more lenient threshold, we find six extra neurons, that when combined with our original 28 neurons, explain 100% of Llama’s performance for addition. These neurons appear to behave similarly to the ones we studied in-depth in the main text (based on activation patterns and alignment with Fourier probes). 
