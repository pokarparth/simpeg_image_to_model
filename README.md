# simpeg_image_to_model
Create a SimPEG model given an image
Trying to recreate this GIFTools utility <https://giftoolscookbook.readthedocs.io/en/latest/content/recipes/other/imageInInversion.html>

Intented for quick forward simulations given a synthetic example or geologic plan-map or cross-section. The function uses a default Tensor mesh if no external mesh defined.
Uses scikit-learn Kmeans to identify clusters in the image so they can be used to define a physical property to each cluster. 
As such, currently does not work for cases where cluster is non-trivial -- e.g., if there are any annotations on the image.

TODO: 
- Account for topo/air.
- Account for padding cells.
- Other mesh types.
- 
