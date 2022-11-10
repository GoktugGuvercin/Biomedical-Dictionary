# Biomedical-Dictionary

### Brain atrophy: 

Brain antrophy, also called as cerebral atrophy, is generally described as the loss of neurons and the deficiency of connections between the neurons. In this case, the brain tends to shrink and its functionalities get weaker. Alzheimer and alcoholism are top-two diseases that directly results in brain atrophy.

### Optical Coherence Tomography

Optical Coherence Tomography (OCT) is one of the medical imaging modalities commonly used by ophthalmologist. As a non-invasive approach, it generates cross-sectional images of the retina in micrometer-resolution between 20-5 $\mu m$ by using low-coherence light. Segmentation of OCT images has an important role on the diagnosis and treatment of different eye diseases like age-related macular degeneration (AMD) and diabetic macular edema (DME).

### Oncogene: 

Proto-oncogenes are particular group of genes in responsible for regulating cell-growth and cell-division. These genes help the cells to grow and divide properly so that they can stay alive and generate new cells. When a proto-oncogene is modified in a way that it is constantly turned on (activated) even when it is not supposed to be, it becomes an oncogene. In this case, the cell grows and divide out of control, which results in cancer. In other words, an oncogene is a type of modified gene that has the potential to cause cancer. *Mutations*, *epigenetic changes*, and *chromosome rearrangements* are three main factors that convert proto-oncogenes into oncogenes.

  
### Tumor Suppressor Genes:

These genes try to restrain uncontrollable cell-growth and division. To be more specific, they keep the cells from dividing too quickly; they slow down cell division process. Sometimes, these suppressors can initiate apoptosis, which means programmed cell death, to keep our cells in a balance. Genetic variants and mutations on tumor suppressor genes may lead them to malfunction or completely stop working. In this case, cell division can get out of the control. In other words, they are strong candidates against carcinogenesis; hence, these genes are also called as anti-oncogenes. From that perspective, tumor suppressor genes and apoptosis have an important role on the prevention of cancer. 

### Partial Volume Effect:

Partial volume effect is generally categorized as a type of artifact observed in 3D medical imaging modalities. In volumetric images, 3D continuous objects such as brain or heart is represented by discrete limited amount of voxels. At that time, multiple tissues may contribute to intensity value of a voxel. In other words, more than one tissue correspond to same voxel, so the intensity of that voxel becomes mixed. This causes blurring of intensity values on tissue boundaries. Thinner slicing can be useful to alleviate this problem. 

### Intensity Inhomogeneity

Intensity inhomogeneity is the situation when intensity values tend to vary instead of being static. In this case, same tissue type can be illustrated with different tones of intensity values. For example, some parts of gray matter in the brain get closer to white color in the scan. This causes shading artifact to appear over the image, which reduces the performance of medical imaging methods that assume the intensity of a tissue class is constant over the range of the image.

Many image processing tasks based on MRI scans like segmentation and registration are strictly dependent on the quality of the images, because they use intensity values as a principal feature. These tasks are vulnerable to intensity inhomogeneity (IIH), also known as the bias field or gain field.

Intensity inhomogeneity is commonly observed in MRI scans, and in general it is caused by the presence of non-uniformity in the radio-frequency (RF) coil. Histogram equalization is one of the methods that can be used to solve this problem; however, it also tend to increase the noise in MRI scans. 7-Tesla and 9-Tesla MRIs generate higher resolutional images, but intensity inhomogeneity comes up as a tradeoff. 

### Image Geometry:

Image geometry is very important to segmentation and registration. In segmentation, segmented voxels of every tissue type is multiplied by the size of one voxel to compute entire volume. At this point, the voxels can be of isotropic or anisotropic. 

- **Isotropic voxel:** voxel of same length in every dimension
- **Anisotropic voxel:** voxel of different length in its dimensions

One of the main reasons why anisotropic voxels are used is awfulness of patients. In purpose, longer voxels through the depth axis are used to reduce scanning time. This is called "Manhattan voxels". 

#### Limited Contrast:

Limited contrast is one of the problems that can directly affect the performance of medical imaging segmentation techniques. Different tissues might have similar physical properties, so they can be illustrated with similar intensity values in imaging modalities. In this case, differentiating adjacent but different tissue types becomes harder. Purely intensity-based segmentation algorithms such as region growing are prone to leak into adjacent tissue. 
