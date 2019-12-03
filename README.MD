# KITTI_eval_offline
Evaluate detection model on KITTI offline using 40 recall positions as proposed in MonoDIS [1].

## How to use
1. Complie `evaluate_object_offline.cpp`.
```bash
g++ -O3 -DNDEBUG -o evaluate_object_offline evaluate_object_offline.cpp
```
2. Prepare label and detection results.
```plain
kitti_eval_offline/
├── label_2/
└── results/
     └── data/
```
3. Run the evaluation code.
```bash
./evaluate_object_offline ./label_2/ ./results/
```

A simple example is provided in `test_eval_offline.py`

## Reference
[1] Andrea Simonelli, Samuel Rota Bulo, Lorenzo Porzi,
Manuel Lopez-Antequera, and Peter Kontschieder. Disentangling monocular 3d object detection. In ICCV, 2019. 