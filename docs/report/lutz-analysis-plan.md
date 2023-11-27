{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "9d3bed2d-544f-48ac-b22a-f3eaa9a156eb",
   "metadata": {},
   "source": [
    "# Planned revisions to reproduction of Kang et al. 2020\n",
    "\n",
    "Authors: Alana Lutz and Elise Chan\n",
    "\n",
    "## Analysis\n",
    "\n",
    "We plan to modify the study by improving speed limit information.\n",
    "In the original study design, most of the road segments do not have speed limit information, and by default they are all set to 35 mph.\n",
    "This could introduce a major inaccuracy, since many roads do not have a 35 mph speed limit.\n",
    "We will improve the study design by replacing the network_setting function with the use of the osmnx.speed module, which calculates speeds for all edges in a graph using the mean speed of the edges of each highway type.\n",
    "For example, all residential road segments with unknown speed limit values will be assigned the mean speed limit of all residential road segments with known speed limit values.\n",
    "The osmnx. speed module can also be used to calculate travel times.\n",
    "\n",
    "\n",
    "## Results\n",
    "\n",
    "To compare and interpret results, we will note how the modification changes the speed limit data checks before & after applying the network_setting function.\n",
    "The data checks display all the unique speed limit values and count how many network edges (road segments) have each value.\n",
    "We will also compare the final spatial accessibility map from our modification to that of the original reproduction in order to interpret how our modification affected the final output.\n",
    "\n",
    "\n",
    "## Discussion\n",
    "\n",
    "If the data checks show that there are substantially different numbers of road segments with different speed limits than the original reproduction, we will know that applying the osmnx.speed module significantly improved speed limit data.\n",
    "In addition, if the final spatial accessibility map appears noticeably different from the original, we will know that this modification is important for the overall outcome of the study."
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.12"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
