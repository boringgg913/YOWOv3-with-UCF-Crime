# YOWOv3-with-UCF-Crime

# 1. Dowload this repository
   git clone https://github.com/boringgg913/YOWOv3-with-UCF-Crime.git
   
# 2. Preprocess the dataset
   ## 1. Dowload the dataset
   ## 2. Cut all videos in the dataset into pictures, one picture per frame
     python split_to_images_test_traverse.py
   ## 3. Perform human detection on a specified segment (frame number) of a video
     python detect_person_target.py
   ## 4. Classify the training set and test set, and the ratio of training and test set for each action is 9:1
     python build_train_test.py
   ## 5. Create two txt files, trainlist01.txt and testlist01.txt, which contain all the pictures of the selected movie.
     python build_split.py
   
# 3. About training
  ## 1. Modify the YAML file
  ## 2. Start trainging
     python main.py --mode train --config config/ucfcrime_config.yaml
     
# 4. Other instructions
   ## 1. evaluation
      python main.py --mode eval --config config/ucfcrime_config.yaml
   ## 2. detecting
      python main.py --mode detect --config config/ucfcrime_config.yaml
