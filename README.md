Neural Network Visualization
============================

You can view this interactive visulization at https://acruikshank.github.io/ml-003-visualization/. This is an attempt to better understand what's going on in the hidden layer of a neural network trained to discriminate between handwritten digits.

Use
------------------
After loading the page in a modern browser, draw a single digit number (0-9) in the gray box at the top. As you draw the visualization will change as it interprets the evolving drawing. The result is the circled digit at the bottom.

Interpretation
------------------
The funny-looking gray squares in the middle represent the theta values that weight the input values going into the hidden layer. The input is a 20x20 square of pixels derived from the drawing, and there are 25 sets of weights corresponding to the 25 nodes in the hidden layer. As you draw, the squares will fade in and out depending on how well the current drawing fits the weights. If the white parts of the drawing coincide with brighter pixels in the square (higher positive weights) the activation value for that node will be closer to 1 and the square will be drawn darker. If the drawing coincides with darker pixels (more negative weights), the activation will be closer to 0 and the square will be almost transparent.

The network of lines drawn between the squares and the digits at the bottom represent the theta2 values that weight the activation values of the hidden layer when used as inputs to the output layer. The brightness represents the activation value of hidden layer node from which it emanates multiplied by the absolute value of theta 2 weight into the output layer. The line will be blue if the weight is negative and orange if it's positive. The dots above the digits represent the sum of all the weighted inputs to the output layer. Blue indicates most of the inputs are negative, orangish-red suggest the inputs are mostly positive, and purple means they are somewhere in the middle.

The opacity of each digit represents the activation value for the corresponding output layer node, and the circled digit is the one with the highest activation value.
