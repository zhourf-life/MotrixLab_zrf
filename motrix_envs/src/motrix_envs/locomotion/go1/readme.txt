1. 环境预览
uv run mxpython scripts/view.py --env go1-flat-terrain-walk
2. 开始训练
uv run scripts/train.py --env go1-flat-terrain-walk
3. 查看训练进度
uv run tensorboard --logdir runs/go1-flat-terrain-walk
4. 测试训练结果
uv run mxpython scripts/play.py --env go1-flat-terrain-walk


1. 环境预览
uv run mxpython scripts/view.py --env go1-rough-terrain-walk
uv run mxpython scripts/view.py --env go1-stairs-terrain-walk
2. 开始训练
uv run scripts/train.py --env go1-rough-terrain-walk
uv run scripts/train.py --env go1-stairs-terrain-walk
3. 查看训练进度
uv run tensorboard --logdir runs/go1-rough-terrain-walk
4. 测试训练结果
由于粗糙地形场景中同时生成了了一个无限大平面和一个崎岖地形高度场，测试训练结果时会仿照训练过程先将智能体生成在平面上，完成一轮行走后再生成到崎岖地形上。用户需要主动调整相机视角和位置来观察智能体的状态。

uv run mxpython scripts/play.py --env go1-rough-terrain-walk
uv run mxpython scripts/play.py --env go1-stairs-terrain-walk