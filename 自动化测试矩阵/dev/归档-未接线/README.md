# 归档：未接线的排查脚本

这 12 个脚本是历次真机排查时的现场工具，**没有被 `run.sh` 引用**（run.sh 只推送并调用
上层目录里的 snap / apply / logtail / softreboot / touchskip / rmmod_only / devver /
racesnap / concurrent / route 共 10 个）。

- 它们多数针对特定一次的故障现场（`decisive*`、`repro_rmmod`、`debug_target`），
  或已被矩阵用例覆盖（`chkstate`/`readstate` 的检查进了 snap，`set.sh` 的功能进了 apply.sh）。
- 保留在此仅供手工排障时参考；运行前先读各文件头注释，确认与当前模块版本的接口一致
  （部分脚本写于 v10.x，引用的参数名可能已变）。
- 判定规则见矩阵 README：「本目录只有一个测试入口：`run.sh`」。
