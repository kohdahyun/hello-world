import os

path_to_train_dataset_1 = os.path.join('datasets','mnist_train.csv')
path_to_train_dataset_2 = os.path.join('datasets','mnist_train_2.csv')
path_to_test_dataset = os.path.join('datasets','mnist_test.csv')

paths_to_datasets = os.path.join('datasets','*.csv') # Returns list of paths


import os
import csv

path_to_train_dataset_1 = os.path.join('datasets','mnist_train.csv')
path_to_output = os.path.join('datasets','mnist_train_cloned.csv')

output_file = open(path_to_output, 'w')
csv_writer = csv.writer(output_file)
csv_writer.writerow(['Label', 'Pixel 1',' Pixel 2'])
with open(path_to_train_dataset_1, 'r') as csv_file:
    reader = csv.reader(csv_file)
    for row in reader:
        print(row)
        csv_writer.writerow(row)

output_file.close


import os

output_path_train = os.path.join('outputs', 'train')

if not os.path.exists(output_path_train):
    os.makedirs(output_path_train)
