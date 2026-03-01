@midscene/shared 的 cli-runner.mjs 会加载 cwd 下的 .env，但这只在 CLI 模式（如 npx midscene）下触发。直接用
  npx tsx 运行脚本时，不会走 CLI runner 路径，所以 .env 不会被自动加载。需要在脚本中手动加载 .env，可以用更轻量的方式—-Node.js 内置的 --env-file 参数。
