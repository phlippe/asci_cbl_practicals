.. notebook_test documentation master file, created by
   sphinx-quickstart on Sat Jul 25 11:56:56 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to the ASCI Computer Vision by Learning course!
=======================================================

| *Course website*: http://computervisionbylearning.info/
| *Course edition*: May, 2022
| *Repository*: https://github.com/phlippe/asci_cbl_practicals/
| *Author*: Phillip Lippe

-----

**UPDATE (May 11)**: To reduce the workload, we decided that each group only has to do Practical 1-3, and choose between Practical 4 **or** Practical 5, but don't require to do both. Each group can individually choose one of the two advanced practicals based on their interests, and are allowed to skip the other practical.

-----

This website provides you access to the content that we will use for the practical session at the ASCI course "Computer Vision by Learning".
In the course, you will conduct 5 practicals to different topics in the domain of machine and deep learning for Computer Vision, with increasing complexity to recent research topics in the field.
Throughout the course, you will be guided by Teaching Assistant that help you with any question you may have.
The teaching team consists of: Adeel Pervez, David Knigge, David Zhang, Tao Hu, Yunhua Zhang, Zenglin Shi, and Phillip Lippe.

The practicals require familiarity with the Deep Learning framework "PyTorch" and common scientific computing packages of Python such as numpy. 
If you are not familiar with PyTorch or would like to have a refresher, please check out our tutorial *Introduction to PyTorch* before the course.
Additionally, the practicals will require you to train several deep learning models.
While we tried to reduce the computational cost of each training as much as possible, you will require access to a GPU in order to finish the practicals.
For more details, please check the instruction in the section *How to run the notebooks*, and make sure to have your preferred solution setup and ready to go at the start of the course.

The practicals are intended to be solved in **groups of 2 students**. 
You can already find team mates before the course starts if you know fellow students, or form the groups during the first practicals.
Once you have formed groups, please sign up your group in `this Google spreadsheet <https://docs.google.com/spreadsheets/d/1H1zmIPaep4_4YFX5aS2h_-H6OQFIIGfzHoLztXWD_-k/edit?usp=sharing>`_.

For any remaining questions regarding the practicals, please contact us at p.lippe@uva.nl.

Schedule
--------

+------------------------------------------+---------------------------------------------------+
| **Date**                                 | **Practical**                                     |
+------------------------------------------+---------------------------------------------------+
| Monday, 9. May 2022                      | Practical 1: Multi-Layer Perceptrons              |
|                                          |                                                   |
| Tuesday, 10. May 2022                    | Practical 2: Convolutional Neural Networks        |
|                                          |                                                   |
|                                          | Practical 3: Vision Transformers                  |
+------------------------------------------+---------------------------------------------------+
| Wednesday, 11. May 2022                  | Practical 4: Regular Group Convolutions           |
+------------------------------------------+---------------------------------------------------+
| Thursday, 12. May 2022                   | Practical 5: Self-Supervised Contrastive Learning |
+------------------------------------------+---------------------------------------------------+

The 5 practicals are aligned with the lectures of each day. 
For the first two days, it is expected that you finish the first three practicals.
Ideally, you would finish Practical 1 and start with Practical 2 on Monday, and finish Practical 2 as well as Practical 3 on Tuesday.
For the remaining two days, one practical per day is scheduled which aligns with the first lecture of each day.
On each day, we have a practical session in the Hotel Casa from 13.30-17.00, where TAs will be in the room to answer your questions.

How to run the notebooks
------------------------

On this website, you will find the notebooks exported into a HTML format so that you can read them from whatever device you prefer.
Your task is to fill in the notebooks to solve the practicals.
There are three main ways of running the notebooks we recommend:

- **Locally on GPU**: If you have a laptop with a build-in NVIDIA GPU, we recommend that you run the practicals on your own machine. All notebooks are stored on the github repository that also builds this website. You can find them here: https://github.com/phlippe/asci_cbl_practicals/. While Practical 1 can be executed on common laptops without a GPU, the later practicals require access to a GPU to keep the training times in a reasonable range. Nonetheless, if you prefer, you can code and test most of your code on a CPU-only system, i.e. your own laptop, and once your code is tested and ready, use one of the remaining options to train the model. To ensure that you have all the right python packages installed, we provide a conda environment in the `same repository <https://github.com/phlippe/asci_cbl_practicals>`_.

- **Google Colab**: If you do not have access to a GPU on your local machine, you can make use of `Google Colab <https://colab.research.google.com/notebooks/intro.ipynb#recent=true>`_. Google Colab provides you access to GPUs for free, and you can activate the GPU support by :code:`Runtime -> Change runtime type -> Hardware accelerator: GPU`. Each notebook on this documentation website has a badge with a link to directly open it on Google Colab. It is highly recommend to copy the notebook to your own Google Drive before starting, since when closing the session, changes might be lost if you don't save it to your local computer or have copied the notebook to your Google Drive beforehand. In addition, note that for free account, Google Colab is limited to one session at a time, and each session has a time limit.

- **Compute cluster**: If you have access to a compute cluster, we recommend to using it to do your final trainings. Depending on your preference, you can implement the practicals either locally or on Google Colab. Once your notebook is ready, you can first convert the notebooks to a script using :code:`jupyter nbconvert --to script ...ipynb`, and then start a job on the cluster for running the script. A few advices when running on clusters:

   - Disable the tqdm statements in the notebook. Otherwise your slurm output file might overflow and be several MB large.
   - Comment out the matplotlib plotting statements, or change :code:`plt.show()` to :code:`plt.savefig(...)`.


Report submission
-----------------

| *Submission email*: asci.cbl.practicals@googlemail.com
| *Deadline*: 31. May, 2022 (23:59 CEST)

At the end of the course, you are expected to submit a report about your findings of your practicals. The report should be prepared as a PDF in the LaTeX template provided in the repository at `report/`. In the report, you are expected to answer the questions in the practicals, and include any figures requested in the practicals (e.g. the training and/or evaluation curves of a model). Your report should have roughly 1 page per practical, with a maximum of 8 pages. For submission, add your report to your filled notebooks as a zip file and send it to asci.cbl.practicals@googlemail.com. Please make sure to **clear all outputs of the notebooks** before submitting, and **exclude any datasets or trained models from your submission**.

Please remember that we do not allow any form of plagiarism. Any plagiarism will lead to all team members failing the course.


.. toctree::
   :caption: Practicals
   :maxdepth: 2

   notebooks/Introduction_to_PyTorch.ipynb
   notebooks/1_MLPs.ipynb
   notebooks/2_CNNs.ipynb
   notebooks/3_Vision_Transformers.ipynb
   notebooks/4_Regular_Group_Convolutions.ipynb
   notebooks/5_Self_Supervised_Learning.ipynb