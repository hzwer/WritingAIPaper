[知乎链接](https://www.zhihu.com/question/347847220/answer/26536819499)

When reviewing papers or reading them, I have become aware of numerous not good practices, and I wish to document these.

### Computational Power Overwhelming

1.1 Increase the batch size to seemingly align the number of iterations.

1.2 Train for more epochs without explicitly stating it, report the training duration in terms of iterations instead of epochs, or vice versa, to obscure the lack of alignment.

1.3 Keep the number of epochs constant but reuse samples multiple times to cover more data surreptitiously.

1.4 Reduce the downsampling frequency in the model, increasing the computational load significantly, yet only compare parameter counts with others.

1.5 Pile on computational power in domains where computational load and parameter count are disregarded.

1.6 Briefly mention high-computation components and only analyze the efficiency of other components.

1.7 Use reparameterization to inflate the model size, making training slower but disregarding the inference overhead.

1.8 Employ EMA (Exponential Moving Average) or model ensembles to boost performance, and if possible, self-distillation.

1.9 Select an extremely small training set, allowing focus solely on overfitting.

### Hyperparameters

2.1 Manipulate experimental results by switching between cosine learning rate schedules and fixed learning rates (the latter stages of cosine schedules often lead to rapid performance gains, so prematurely reducing the learning rate can make training appear more efficient).

2.2 Slightly increase the learning rate while decreasing the baseline's learning rate.

2.3 Conceal various hyperparameters within the code as "magic numbers."

2.4 Cherry-pick random seeds.

### Minor Tweaks

If one tweak is important, it should be stated in the paper. Many papers conceal their tweaks.

3.1 Replace all ReLU activations with Swish or Leaky ReLU/PReLU.

3.2 Add SE (Squeeze-and-Excitation) layers throughout the model, as they generally improve performance; incorporate inexpensive attention connections.

3.3 Replace parameter-free components like pooling and resizing with learnable ones to gain extra capacity.

3.4 Arbitrarily add skip connections between modules and concatenate additional features, as it rarely hurts.

3.5 Add Batch Normalization (BN) where it's absent, remove it where it's present, or experiment with other normalization techniques like Group Normalization (GN), Instance Normalization (IN), Layer Normalization (LN), or Weight Normalization (WN).

3.6 Augment the training set to align with the test set distribution, altering the training set's characteristics.

### Incremental Designs

4.1 Incorporate peculiar GAN losses or consistency losses, which are difficult to assess but can fill pages with formulas.

4.2 Elaborate on techniques mentioned briefly in others' papers, adding "magical" formula transformations to extend the manuscript.

4.3 When designing a new component x, create a learnable parameter beta initialized to 0, and add beta * x to the model instead of x alone. In the worst case, beta remains 0, leaving the model unchanged.

4.4 Extend the previous point by designing multiple components and combining them with learnable parameters.

4.5 Further extend by incorporating Neural Architecture Search (NAS).

4.6 Utilize pre-trained parameters from other models to elevate the starting point and potential upper bound of the model, akin to adding more data and annotations.

4.7 Implement complex curriculum learning or elaborate distillation techniques (feature-level, cross-modal, etc.). If others struggle to reproduce the results, attribute it to the need for hyperparameter tuning.

4.8 Regardless of utility, apply a reinforcement learning framework to imbue the model with more autonomy.

### Evaluation Methods

5.1 Measure ten metrics but only report the three showing improvement.

5.2 Conduct experiments on ten datasets but discard the five without favorable results.

5.3 Deliberately misalign the testing method with others' training scenarios to lower the baseline, e.g., inverting RGB channels to sabotage competitors.

5.4 Invent novel evaluation metrics or modify existing ones, such as measuring PSNR on the Y channel while comparing it to RGB measurements.

5.5 Identify trivial yet overlooked scenarios to demonstrate substantial improvements.

5.6 Compare a large model against others' smaller models without reporting their larger counterparts, or compare a model trained for a specific metric against untrained ones.

5.7 Test on different hardware and report the results together.

5.8 For recent large language models, surreptitiously add hints to test prompts, comparing few-shot and zero-shot performance.

5.9 Indirectly overfit to the test set by leaking data or random seeds, or include test samples in upstream pre-training.

5.10 Introduce real-world scenarios or out-of-distribution (OOD) samples to the test set, causing significant drops in baseline performance. Then, apply augmentations or dropout to recover the lost performance, attributing the gains to other factors.

5.11 Use private test sets with subjective human judgment, allowing arbitrary claims of improvement.

5.12 If objective comparisons fail, resort to subjective ones, and if subjective comparisons fail, selectively present favorable results (cherry-picking).

### Ultimate Methods

6.1 Replicate someone else's method but rename it entirely.

6.2 Report high performance but only provide a README when asked for the source code.

6.3 Begin writing the paper without conducting experiments, conveniently surpassing the state-of-the-art by a narrow margin.

**Reiterating, the above are cautionary examples meant to serve as a guide against deceptive practices.**
