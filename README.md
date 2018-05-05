# data_visualization

参见自己的网站http://ghost2876.github.io   内有Force-Directed Layout 力导向图的实现。

先计算所有vertices之间的repulsive forces，然后计算有edge关联的vertices之间的attractive forces，然后lower the temperature（就是减小下次iteration时移动vertices displacement的位移量step size）。这样当若干次之后整个graph进入稳态（stable status）具备minimum force（最小能量）。使用的是模拟退火算法simulate annealing algorithm

整个目的是让有edges关联的点能尽可能在一起，而没有关联的则闪到一边，实现一种初步的“聚类”，减轻普通graph layout的edges大量交叉a massive的问题。

参见CS560 Data Visualization课程目录A3_Introduction_to_Graph_Layout_Algorithm文件夹下的论文force-directed.pdf
