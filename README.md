# ChunKin_FaceRecognition

The focus of this project is to compare the extracted features with the facial image database in order to use openCV for recognition and analysis. Another goal of face recognition is to find a series of data of the same face in a set of training images in the database from the incoming image. The biggest difficulty is to make this process happen in real time, not all biometric facial recognition software providers can use it. Below is the command line to run them:

cd C:\Users\60169\Documents\RDS_Y2S1\AI_Assignment\ChunKin_FaceRecognition

python extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7

python train_model.py --embeddings output/embeddings.pickle --recognizer output/recognizer.pickle --le output/le.pickle

python recognize.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle --image images/chunkin.jpg


python recognize_video.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle
