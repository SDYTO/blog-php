# Read Me

## 项目概述

本项目是一个无需数据库支持的博客系统，旨在通过减少对数据库的依赖来提升页面加载速度并节省服务器性能。

## 功能特点

- **无需数据库**：博客内容直接存储在`blog.txt`文件中，无需数据库支持。
- **内容管理**：通过`write.php`页面，博主可以发布新的博客内容和管理已有博客（包括发布和删除）。
- **密码验证**：发布和删除博客内容时需要密码验证，初始密码为`root`，可在`write.php`文件的第三行`$correctPassword = 'root';`处自行修改。
- **内容存储**：博客内容（包括标题、发布时间和内容）存储在`blog.txt`中。
- **页面展示**：用户访问`blog.php`时，该页面会调用`load_blog.php`来获取`blog.txt`中的内容，并按照格式显示在页面中。
- **响应式设计**：通过媒体查询判断设备类型，并使用不同的CSS适配手机和电脑。

## 部署指南

1. **下载源文件**：直接下载本项目的所有源文件。
2. **上传至服务器**：将下载的源文件上传至您的服务器。
3. **配置密码**：在`write.php`文件中，将`$correctPassword`的值替换为您希望设置的密码。
4. **访问博客**：通过浏览器访问`blog.php`来查看博客内容。

## 快速编辑

- **直接访问编辑页面**：博主可以直接在自己的域名后面输入`/dev.html`即可快速的前往编辑页面。

## 文件结构

- `blog.php`：博客首页，用于展示博客内容。
- `load_blog.php`：用于从`blog.txt`加载博客内容的脚本。
- `write.php`：博主用于发布和管理博客内容的页面。
- `blog.txt`：存储博客内容的文本文件。

## 注意事项

- 请确保服务器支持PHP语言环境。
- 在部署前，检查所有文件的权限设置，确保服务器可以正确读取和写入文件。
- 定期备份`blog.txt`文件，以防数据丢失。
