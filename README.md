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

### Limited Contrast:

Limited contrast is one of the problems that can directly affect the performance of medical imaging segmentation techniques. Different tissues might have similar physical properties, so they can be illustrated with similar intensity values in imaging modalities. In this case, differentiating adjacent but different tissue types becomes harder. Purely intensity-based segmentation algorithms such as region growing are prone to leak into adjacent tissue. 

### Diagnosis of Brain Tumors: 

Brain MRI is directly used in the diagnosis of brain tumors. For the detected tumors, a 2-steps process, both of which requires MRI scan, is conducted:

- Surgical and radiation treatment planning
- Treatment response evaluation

Working with 3D MRI in deep learning is computationally expensive. Hence, one recommended approach is to divide the images into local patches. At this point, understanding relational dependencies between different brain regions and consideration of brain connectivity information have an important role in the diagnosis of tumors by semantic segmentation. Graph neural networks seem to be the most suitable technique for this:

- It can incorporate local and global connectivity into model predictions. It achieves to do this by the aggregation of information shared by neighboring nodes. 
- It can capture relational information between cortical brain regions.

### Folate and Its Relationship with Cancer:

Folate is vitamin B9 and it is essential to fundamental cell processes. It is used in the metabolism of amino-acids for cell division. 
It has an important role in DNA synthesis and DNA reapir. Rapidly dividing cells like cancer need to have huge amount of folate. Folate receptor is responsible for binding and transporting folate into cells. There are 3 major types of folate receptor: FOLR1 - FOLR2 - FOLR3

If FOLR transporters are over-expressed (generated) in a specific tissue type, this means that this tissue needs so huge amount of folate molecule, which is the indication of cancer in that tissue. In other words, FOLR is proposed to promote cancer by increasing folate tranporting. Over-expression of FOLR1 can be identified in epithelial tissue segmentation.

### B7H4 and Its Relationship with Cancer:

B7 is a type of membrane protein which binds to biological membranes permanently. Glycophorin and Rhodopsin are well known membrane proteins observed in red blood cells and rod cells of retina respectively. T-cells are a type of white blood cells as promoter to immune system.

The most famous B7 protein is B7-H4 which is capable of reducing the effect and response of T-cells in human body. It is obverted that over-expression of B7-H4 triggers many cancer types like breast, prostate and colorectal cancer by negatively regulating T-cell immunity.
In normal tissues, B7-H4 molecule rate is limited, but in malignant tumors and the tissues infected with cancerogenesis, it is quite a lot. Hence, B7-H4 is considered as a potential diagnostic and prognostic biomarker in many cancer types.

Over-production of B7H4 induces epithelial-mesenchymal transition (EMT), which is a biological process that causes cells to lose polarity, adhesion and gain migratory properties. In this case, epithelial tissues tend to go through canceroginesis, invasion, and metastasis. Epithelium segmentation tries to analyze EMT and correlates it with B7H4 membrane protein in deep learning.

### PTEN and Anti-Cancer Drugs:

PTEN is a specific type of enzyme generated in human body as a part of phosphatase protein product. It is in charge of cell cycle regulation to avoid fast growing and constant dividing processes of cell structure. That is why it is commonly used as an ingredient of anti-cancer drugs and PTEN gene is evaluated as tumor suppressor gene. The lack of PTEN as a result of mutation in PTEN gene can trigger prostate cancer (PCa), lung cancer and breast cancer. Rapid loss of PTEN accelerates cancerogenesis, which directly impacts epithelial tissue. Epithelium segmentation in histopathological images of prostate or breast tissues generally targets on grading of cancer level and quantification of loss in PTEN level.

### PD-1 and PD-L1 Proteins:

PD-1, standing for programmed cell death 1, is a type of protein commonly observed on the surface of T and B cells.  The main role of this protein is to down-regulate immune system. In other words, it surpasses the power and inflammatory activity (generating a response against possible offending agent like viruses, bacteria or toxic chemical) of immune system partially. By doing this, many kinds of autoimmune diseases (diseases that occur because of immune system's mistakenly targeting on healthy tissues in the body) can be avoided by PD-1 protein, so it would promotes self-tolerance. 

However, PD-1 is also capable of preventing immune system from killing cancer cells. The protein PD-L1 is dominantly expressed on cancer cells, and interaction of PD-1 with PD-L1 (binding by affinity) can hide cancer cells from immune system, so cancerogenesis in human body get a chance to accelerate its formation. At the end, cancer cells become capable of invading immune system. PD-1 inhibitors are specifically used to prevent the binding and interaction between PD-L1 and its receptor molecule PD-1, which is called cancer immunotherapy. PD-L1 expression and diagnosis of cancerogenesis can be detected by image segmentation on epithelial tissues with the help of deep learning. 

### Confusion Matrix:


|                 | `Cond Positive` | `Cond Negative` |
| ---             |     ---         |      ---        |
| `Pred Positive` |  True Positive  |  False Positive |
| `Pred Negative` | False Negative  |  True Negative  |

* TP: Correctly Diagnosed Patients (Hits)
* TN: Correctly Diagnosed Healthy Subjects (Correct Rejections)
* FP: False Alarm (type-1 error, causing wrong treatment to be applied to healthy subject)
* FN: Missing a disease (type-2 error, causing the delay of patient treatment)

Specifically, brain atrophy and breast cancer have a lot of false positive cases. 
