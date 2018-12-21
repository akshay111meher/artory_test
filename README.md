# Artory Test

## How run the code

1) Clone the repository using 
   > git clone https://github.com/akshay111meher/artory_test.git
2) Run to following
    > cd artory_test
3) If you have **Go** already installed in your system skip to step 5.
4) If you dont have **Go** installed in system you can run it docker container.
    1) Start the docker container
        > docker-compose up
    2) This will pop up message like this
        ![alt text](https://github.com/akshay111meher/artory_test/blob/master/pictures/docker.png)
    3) In another terminal run the following
        > docker exec -it sample_container /bin/bash
    4) This is shell where we can run our code.

5) To test the sample cases and sample input provided in the problem statement. Run the following
    > go test
This will run the test cases and show the output
![alt text](https://github.com/akshay111meher/artory_test/blob/master/pictures/test.png)

6) To run the main program
    > go run phone_number_success_rate.go

The sample that I have used has around 3000 entries, however if you want to test it with your own data, start the code in **step 6** by
  > go run phone_number_success_rate.go <relative_path_to_file>

For example, if **sample.csv** is the input file that you wish to provide, you can run the code in **step 6** by
  > go run phone_number_success_rate.go sample.csv

if no input file is provided, then **data/data.csv** will be taken as input

## Notes

   1) Instead of passing data as a string, I have decided to pass it as through file pointer (**logadata**), as with strings the code looks awful, when strings become large.
   2) I have written the code in **Golang** as I am comfortable with it and in built testing packages. However, if you demand, I can share the same in **Node.js** and **Python** also.
   3) It is expected that docker and docker-compose are already available as they are industry standards for containerization
   4) If you are using docker to run, then in **Step 4.1** you may encounter a prompt for building the image locally. You can press **y** to continue the process.
