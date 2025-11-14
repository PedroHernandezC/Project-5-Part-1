# Project 5 -- Part 1 -- The Batch-then-drain trace
## Student Information: 
**Name**: Pedro Hernandez Carranza 

**Student ID**: 008806974

**Repository Link**: https://github.com/PedroHernandezC/Project-5-Part-1

## Reflection
This project was quite interesting and different from the others. This project required far more understanding of someone else code as well as being able to add to it. The program also has many layers that either interact directly or indirectly with the main program, harness. Understanding these interactions and how they were implemented took some time. After getting to understand the program the trace generator, batch_the_drain, was added and the harness was modified to include it in the runs as well as generate csvs from both the batch_then_drain and huffman profiles. 
- Collaboration & Sources: 
  - Many of the other students asked some very important questions regarding what should be changed and kept the same. Your responses to them was a great help and assured me i was on the right path.
  - As instructed by "Empirical Analysis of Huffman Profiles" I asked chatGPT several question about the operations being tested as well as about c++ chrono.
  - This portion of the project did not require a lot of programming as the provided coded was heavily used as reference.
  - I used in AI in figuring out how to compile some of the various programs from the command line. While in development I used Clion's Cmake tools to run the programs.
- Implementation Details:
  - Compiling huffman_coding
    - cd into src then trace-generators then into huffman_coding
      - Run the following to compile: g++ -std=c++17 main.cpp -o huffman_trace_generator
      - Execute the following to generate traces: ./huffman_trace_generator
  - Compiling batch_then_drain 
    - cd into src then trace-generators then into batch_then_drain
      - Run the following to compile: g++ -std=c++17 main.cpp -o batch_the_drain_trace_generator
      - Execute the following to generate traces: ./batch_the_drain_trace_generator
  - Compiling harness
    - cd into src then into harness
    - Run the following to compile: g++ -std=c++17 -I . main.cpp ../../utils/comparator.cpp ../implement
ations/BinaryHeapInVector/BinaryHeapInVector.cpp ../implementations/BinomialQueues/BinomialQueue.cpp ../implementations/
BinomialQueues/BQnode.cpp ../implementations/LinearBaseLine/LinearBaseLine.cpp ../implementations/Oracle/QuadraticOracle
.cpp -o harness
    - Execute the following to generate traces: ./harness

- Testing & Status:
  - Generated traces were checked for formatting issues and then later the generated csvs were also checked for mating issues.
  - I uploaded the generated csvs to different instances of the pq_multi_impl_anchor_heap_tooltips.html to see if the expected shape of NlogN.
