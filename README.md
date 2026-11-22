# 我的小站 · hytow.github.io

三个纯静态小应用，托管在 GitHub Pages，无需后端、无需构建。

## 线上地址

| 路径 | 应用 | 网址 |
| --- | --- | --- |
| `ziqu/` | 字趣 · 汉字合体与添笔 | https://hytow.github.io/ziqu/ |
| `auditory-cards/` | 听觉训练卡 | https://hytow.github.io/auditory-cards/ |
| `fruit-slot-8090/` | 花果水果机 · 8090 复刻版 | https://hytow.github.io/fruit-slot-8090/ |

根目录的 `index.html` 是导航页：https://hytow.github.io/

## 目录结构

```
.
├── index.html              导航页（三个入口）
├── ziqu/                   字趣，单文件
├── auditory-cards/         听觉训练卡，单文件
├── fruit-slot-8090/        花果水果机（PWA）
│   ├── index.html
│   ├── manifest.json
│   ├── img/                图片
│   └── snd/                音频
├── README.md
└── .nojekyll               让 Pages 跳过 Jekyll，不要删
```

## 怎么更新

改完这个文件夹里的文件后：

```bash
git add .
git commit -m "说明这次改了什么"
git push
```

约 1 分钟后线上生效。首次推送会弹出 GitHub 登录窗口，授权一次即可。

## 新增一个应用

1. 新建文件夹，例如 `my-app/`，里面放一个 `index.html`
2. 在根目录 `index.html` 里照现有卡片加一个 `<a class="card" href="./my-app/">`
3. 推送后访问 `https://hytow.github.io/my-app/`

## 注意

- 仓库是公开的，不要放密码、密钥、`.env` 这类文件
- 需要构建的项目（React/Vue）要先打包，把 `dist` 里的静态文件放进来
- 需要后端或数据库的项目，GitHub Pages 跑不了，得用 Vercel、Render 之类的服务
