# embryoidNeuralODE
Neural ODE Implementation for Invertible Distribution Transport between an Embryoid Cell Distribution and the Gaussian Distribution


Technical Implementation:

- implements a neural ODE
    
    + utilizes TorchDyn](https://torchdyn.org)
        
- implements the the [`Learner(pl.LightningModule)`][`LightningModule`] [PyTorch Lightning] class
    
    +  transports a gaussian distribution to a cell distribution
    
    + retains invertibility i.e.
        
        - goes from cells to a gaussian and vice versa
        
- inverts generated cells from PCA space to gene space
        
- implements magnitude regularization

    + utilizes [TorchDyn](https://torchdyn.org)

    + references [Tong _et al._ 2020](https://arxiv.org/pdf/2002.04461.pdf)


[PyTorch Lightning]: https://lightning.ai/docs/pytorch/stable/
[`LightningModule`]: https://lightning.ai/docs/pytorch/stable/common/lightning_module.html


Includes the following feature plots:

- PHATE vs PCA
    
    + 1 figure with two subplots, one for each embedding. 
    
    + cells are colored by time.

- generated cells vs real cells in PCA space
    
    + 1 figure
    
    + real cells use a different marker than generated cells
    
    + cells are colored by time

- generated cells vs real cells expression
    
    + 1 figure
    
        - can be 10 subplots (2 rows of 5) 

            + one row for generated 
        
            + one row for ground truth 
            
    + generated data is colored differently than ground truth data

