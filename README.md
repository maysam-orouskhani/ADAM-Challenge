# ADAM-Challenge
Rank 4 in ADAM Challenge Live Leaderboard (Aneurysm Detection And segMentation Challenge) for the Segmentation Task.
Pre-trained Models for Intracranial Aneurysm Segmentation and Detection.

![image](https://user-images.githubusercontent.com/125511615/219178638-08379c49-988e-47ad-95ed-2b270ba6e944.png)

![image](https://user-images.githubusercontent.com/125511615/219178878-55cfbc53-fd9f-4e4c-9b50-8cd96ae59d9c.png)


How to Use: <br />

1- copy a TOF-MRA image into folder "input/pre". <br />

2- Run the follwoing codes: <br />
cd nnUNet    <br />
pip install -e .   <br />
cd ..   <br />
python ADAM_Preprocess.py --input_path ./input <br />

3- Download the models and put them into the follwoing path:  <br />
"nnUNet/nnunet/TrainedModels/nnUNet/3d_fullres/Task101_SCGM/nnUNetTrainerV2__nnUNetPlansv2.1/  <br />

4- Run the follwing codes:   <br />
cd nnUNet/nnunet  <br />
nnUNet_predict -i ../../input_preprocess -o ../../seg_initial -m 3d_fullres -t Task600_ADAM --disable_tta  <br />
cd ../../   <br />

5- Do the post-precessing as follwos:  <br />
python ADAM_Postprocess.py --save_path ./output  <br />

*Find the segmmented image in "output"











