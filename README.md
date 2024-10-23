# simpeg_image_to_model
Create a SimPEG model given an image file to replace need for explicitly defining the indices.

Trying to recreate this GIFTools utility <https://giftoolscookbook.readthedocs.io/en/latest/content/recipes/other/imageInInversion.html>

Intented for quick forward simulations given a synthetic example or geologic plan-map or cross-section. The function uses a default Tensor mesh if no external mesh defined.
Uses scikit-learn Kmeans algorithm to identify clusters in the image so they can be used to define a physical property to each cluster. 
As such, currently does not work for cases where cluster is non-trivial -- e.g., if there are any annotations on the image.

Example:
![image](https://github.com/user-attachments/assets/850a36c7-6101-4739-8350-ea4529861055)


TODO: 
- Account for topo/air.
- Account for padding cells.
- Other mesh types.
