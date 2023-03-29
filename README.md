# Some Key Points from the Deep Learning Tuning Playbook

The points in this summary derive from the "Deep Learning Tuning Playbook" published by Google Research, the original work can be found at [https://github.com/google-research/tuning_playbook](https://github.com/google-research/tuning_playbook) and has a CC BY 4.0 Licence [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/). This content is designed to list some key ideas, please refer to the book for more ideas and details. When referencing, please cite the original playbook. The playbook is an excellent resource for engineers and researchers looking to optimize the performance of their deep-learning models, offering in-depth explanations and best practices for hyperparameter tuning and model training.

## Model Architecture and Optimizer

- Utilizing existing, successful model architectures for new projects.
- Selecting popular optimizers suited for the problem.
- Using the largest batch size supported by hardware for efficient training and resource usage.

## Hyperparameter Tuning and Optimization

- Identifying scientific, nuisance, and fixed hyperparameters.
- Adopting incremental tuning for improved model optimization.
- Ensuring a large enough search space and sufficient sampling.
- Modifying the search space to prevent infeasible trials.
- Assessing trial variance by repeating the best trial N times.
- Balancing exploration and exploitation.
- Using quasi-random search with low-discrepancy sequences for exploration.
- Applying advanced black box optimization algorithms, like Bayesian optimization, during exploitation.
- Utilizing Bayesian optimization tools for final tuning.

## Training, Monitoring, and Adjustment

- Establishing experiment tracking to log crucial experiment data.
- Saving checkpoints and retrospectively selecting the best one.
- Generating training curves for all trials and using various plots for model behavior analysis.
- Reviewing top-performing trials' training curves to evaluate the need for training process refinement.
- Implementing changes that improve results while considering added complexity.
- Optimizing input pipeline by addressing I/O latency, costly pre-processing, and enhancing data prefetching.
- Tackling batch normalization implementation details, especially when altering batch size or host numbers.
- Applying learning rate decay schedules like linear or cosine decay.
- Steering clear of intricate, non-reproducible human-in-the-loop learning rate schedules.
- Determining and applying optimal base learning rate, warmup, and post-warmup steps.
- Employing gradient clipping to address early or mid-training instabilities.
