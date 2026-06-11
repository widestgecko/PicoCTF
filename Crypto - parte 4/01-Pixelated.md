## Descripción

I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled2.png)

## Solución

Uso el siguiente codigo de Python para juntar ambas imágenes. from PIL import Image

def combine_images(image1_path, image2_path, output_path):

    # Open the images

    image1 = Image.open(image1_path)

    image2 = Image.open(image2_path)

    # Ensure both images have the same size

    if image1.size != image2.size:

        raise ValueError("Images must have the same size")

    # Combine the images using a simple averaging technique

    combined_image = Image.blend(image1, image2, alpha=0.5)

    # Save the combined image

    combined_image.save(output_path)

if **name** == "**main**":

    # Provide the paths of the input images and the desired output path

    image1_path = "scrambled1.png"

    image2_path = "scrambled2.png"

    output_path = "combined_image.png"

    combine_images(image1_path, image2_path, output_path)

Nos regresa una imagen en la cual si bajamos el brillo de esta podemos ver la bandera: picoCTF{d562333d}