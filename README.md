# RL_Off_Policy

## Code to Convert

- [x] main.py
- [x] models/networks.py
- [x] algs/A2C/a2c.py
- [ ] algs/OFPG/ofpg.py
- [ ] algs/OFPG/buffer.py
- [x] oailibs/common/misc_util.py
- [x] misc/torch_utility.py
- [x] misc/runner.py

## Questions

- [ ] models/networks.py: [L179](https://github.com/zhanghang1989/RL_Off_Policy/blob/patch-1/models/networks.py#L179), what is the init function doing


## Terminal Commands

please manually set the following environment variables in the terminal, if you'd like to disable cudnn autotune or set cudnn deterministic:

```
export MXNET_CUDNN_AUTOTUNE_DEFAULT=0
export MXNET_ENFORCE_DETERMINISM=1
```
