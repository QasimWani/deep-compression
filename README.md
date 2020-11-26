# deep-compression
Deep Compression utilizing denoising autoencoders

<p> Paper in reference: <a href="https://arxiv.org/pdf/1703.00395.pdf">Lossy Image Compression with Compressive Autoencoders</a>
  
## Autoencoder architecture

![](https://miro.medium.com/max/1056/1*UGFC8BIXEWAqqoxAObJENQ.png)


## Deep Compression - Deep Denoising Compressive Autoencoders (DCAE) - architecture

![](https://www.researchgate.net/profile/Donghoon_Lee19/publication/321895810/figure/fig1/AS:578972472037376@1515049202368/Convolutional-denoising-autoencoder-CDAE-that-was-used-for-denoising-the-chest.png)


## Preliminary Results

#### This was generated using the following architecture (note lack of 'deep' and 'compressive') for 100 epochs
```python

DAE(
  (encoder): Sequential(
    (0): Linear(in_features=784, out_features=256, bias=True)
    (1): ReLU(inplace=True)
    (2): Linear(in_features=256, out_features=128, bias=True)
    (3): ReLU(inplace=True)
    (4): Linear(in_features=128, out_features=64, bias=True)
    (5): ReLU(inplace=True)
  )
  (decoder): Sequential(
    (0): Linear(in_features=64, out_features=128, bias=True)
    (1): ReLU(inplace=True)
    (2): Linear(in_features=128, out_features=256, bias=True)
    (3): ReLU(inplace=True)
    (4): Linear(in_features=256, out_features=784, bias=True)
    (5): Sigmoid()
  )
)

```

![dense layer testing on 100 epochs](assets/preliminary_results.png)
