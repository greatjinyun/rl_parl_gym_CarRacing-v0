# rl_parl_gym_CarRacing-v0

[English Readme](README.md)

尝试利用PARL框架，解决GYM的'CarRacing-v0'问题。

## 环境
```
print(env.observation_space)
print(env.action_space)
Box(96, 96, 3)
Box(3,)
```

## 思路

计划分为三个解决方案
- 方案一
问题最简化，易训练，但跑完一局的时间可能比较长。
默认开局前N帧加速，之后速度保持不变。
这样Agent的决策空间简化为前进，左转，右转，三个离散值。
训练难度下降，但是由于速度不变，不会拿到高分。

- 方案二
方案一的基础上增加动作，训练难度增加，跑完一局的时间应该可以缩短。
增加加速，减速等动作，决策空间增加到七个离散值。
还在训练中。

- 方案三
利用最原本的动作空间训练，目前难以收敛，还需要调整。

## 成果
- 方案一
左转控制比较好，部分右转情况控制还不理想。

![s01_01](resource/output_s01_01.gif)

- 方案二
训练中，敬请期待。

- 方案三
计划中，敬请期待。
