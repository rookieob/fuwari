---
title: first
published: 2026-02-15
description: This is the first post of my new Astro blog.
image: "./cover.jpeg"
tags: [Foo, Bar]
category: 个人博客
draft: false 
lang: ''
---
  
  **这是第一个写的博客，试试看。**

  *看看效果怎么样！*

># **Markdown的部分语法**：
1.1 标题编辑（#的用法，前面为显示，后面为代码输入格式）
# 标题&#12288;&#12288;\# 标题
## 标题&#12288;&#12288;&#12288;&#32;\## 标题
### 标题&#12288;&#12288;&#12288;&#12288;&#32;\### 标题
#### 标题&#12288;&#12288;&#12288;&#12288;&#12288;&#12288;\### 标题   

1.2 正文

直接输入即可。

换行要在代码中空一行，
回车是不会在渲染里显示效果的。
其他还有是用两个空格，或者用``<br>``或者加\然后按Enter键。

1.3 代码块（```）

干IT的少不了和各种代码，命令行接触；Markdown的代码块功能就非常有用了——
代码块通过两行 ``` 符号框出，如果你写的代码是某种语言，那么可以在第一行末尾加上这个语言的名字，代码块内的代码就会执行对应的高亮语法，例如python

```
show ip interface brief
router ospf i
```

```python
print (
  'helld,world'
) 
```

1.4 行内代码（\` \`）

正文中的代码，则通过输入\` \`
框出

比如``show ip interface brief``

1.5 列表

有序列表，输入数字，加一个句点，然后空格即可；可以缩进空置多级列表；

1. 123
2. 456
3. 789
   1. 123
      1. 456 
           1. 789

无序列表，输入 - ,然后空格
- 123
  - 456
    - 789
  
1.6 加粗和倾斜

一个*
加倾斜
两个**
加粗
三个***加粗和倾斜

示例：    
*我们*    
**我们**    
***我们***

># **Fuwari自定义博客参考(src/config.ts)**
config.ts部分配置参考   
站点信息&顶部图
```
export const siteConfig: SiteConfig = {
  title: '你的标题',
  subtitle: '你的副标题',
  lang: 'zh_CN',  // 'en', 'zh_CN', 'zh_TW', 'ja', 'ko'
  themeColor: {  // 主题色部分，按个人喜好配置
    hue: 250,
    fixed: false,
  },
  banner: {
    enable: true,  // 是否开启顶部图
    src: 'assets/images/你的图片',  // 顶部图存放路径
    position: 'center',  //  defaults或者center
    credit: {
      enable: true,  // 是否显示顶部图文本描述
      text: '想显示的文本',  // 输入文本等描述
      url: 'https://xxxxxxxxxxxxx'  // 顶部图的来源url等
    }
  },
```

顶部导航栏github部分    
```
export const navBarConfig: NavBarConfig = {
  links: [
    LinkPreset.Home,
    LinkPreset.Archive,
    LinkPreset.About,
    {
      name: 'GitHub',
      url: 'https://github.com/saicaca/fuwari',  // 想要跳转的url
      external: true,  //是否显示外部链接图标并将在新标签中打开
    },
  ],
}
```

左侧信息页配置    
```
export const profileConfig: ProfileConfig = {
  avatar: 'assets/images/avatar.png',  // 头像图片文件路径
  name: 'AULyPc',     // 你的昵称
  bio: '这片大地...',  // 你的签名
  links: [           // 社交栏配置
    {
      name: 'Twitter',
      icon: 'fa6-brands:twitter',  // https://icones.js.org/ icon图标网站
      url: 'https://twitter.com/AULyPc1',
    },
    {
      name: 'Steam',
      icon: 'fa6-brands:steam',
      url: 'https://steamcommunity.com/profiles/76561198813644850/',
    },
    {
      name: 'GitHub',
      icon: 'fa6-brands:github',
      url: 'https://github.com/AULyPc',
    },
    {
      name: 'Email',
      icon: 'material-symbols:mail',
      url: 'mailto:cecilybenson8@gmail.com',
    },
  ],
}
```
文章Frontmatter   
执行 pnpm new-post <filename> 创建新文章页面后就可以在 src/content/posts/ 目录中编辑你的第一篇文章了。
文章需包含以下内容
```
---
title: My First Blog Post  <!-- 你的文章标题 -->
published: 2023-09-09  <!-- 文章发布时间 -->
description: This is the first post of my new Astro blog.  <!-- 简单描述你的文章，可有可无 -->
image: /images/cover.jpg  <!-- 文章主页的封面，可有可无 -->
tags: [Foo, Bar]  <!-- 文章标签 -->
category: Front-end  <!-- 文章分类 -->
draft: false  <!-- 文文章是否为草稿，默认false；设置为true后部署后不可见，但本地开发预览时仍可见 -->
language: ''  <!-- 可有可无，按需设置 -->
---
```

暂时就这样吧，有空在写。