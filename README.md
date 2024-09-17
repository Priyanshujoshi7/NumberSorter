Number Sorter Project

Overview
This project demonstrates the implementation of several fundamental sorting algorithms using JavaScript. 
Sorting algorithms are essential in computer science, and this project helps visualize how these algorithms work to sort numerical data. 
By building this number sorter, you'll gain a deeper understanding of algorithmic thinking and how to apply it in real-world applications.

Key Features

Implementation of key sorting algorithms:

Bubble Sort: A simple comparison-based algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.

Selection Sort: An algorithm that repeatedly finds the minimum element from the unsorted part and puts it at the beginning.

Insertion Sort: A comparison-based algorithm that builds the final sorted array one item at a time.

Visualization of each algorithm’s step-by-step sorting process.

Allows users to input a list of numbers and see how the algorithms sort them in real-time.

Technologies Used

JavaScript: Core language used to implement sorting algorithms.
HTML/CSS: Used for the user interface and visualization of the sorting process.

Sorting Algorithms Implemented

Bubble Sort:

This algorithm repeatedly compares adjacent elements and swaps them if they are in the wrong order. The process continues until the list is fully sorted.

function bubbleSort(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length - i - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]]; // Swap
      }
    }
  }
  return arr;
}
Selection Sort:

In this algorithm, the smallest (or largest, depending on sorting order) element is selected from the unsorted portion and moved to the correct position.

function selectionSort(arr) {
  for (let i = 0; i < arr.length; i++) {
    let minIdx = i;
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[j] < arr[minIdx]) {
        minIdx = j;
      }
    }
    [arr[i], arr[minIdx]] = [arr[minIdx], arr[i]]; // Swap
  }
  return arr;
}
Insertion Sort:

This algorithm builds a sorted portion of the array, one element at a time. It takes each new element and places it in its correct position among the previously sorted elements.

function insertionSort(arr) {
  for (let i = 1; i < arr.length; i++) {
    let current = arr[i];
    let j = i - 1;
    while (j >= 0 && arr[j] > current) {
      arr[j + 1] = arr[j];
      j--;
    }
    arr[j + 1] = current;
  }
  return arr;
}

How It Works

User Input: Users can input a list of numbers through the interface.

Algorithm Selection: Users choose the sorting algorithm they want to apply: Bubble Sort, Selection Sort, or Insertion Sort.

Real-time Visualization: The sorting process is visualized step by step, showing how the algorithm rearranges the numbers.
