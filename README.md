# 使用GitHub Pages搭建学术个人主页

## 项目结构
- **主页模板**：使用 [academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io) 作为主页模板。
- **同步工具**：使用 [codexu/note-gen](https://github.com/codexu/note-gen) 作为同步工具，用于创建和管理私人仓库，并将本地文件同步到GitHub。

## 步骤概述
1. **克隆主页模板**：
   - 克隆 [academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io) 到本地。
   - 修改本地文件以适配你的个人信息和内容。

2. **配置同步工具**：
   - 使用 [codexu/note-gen](https://github.com/codexu/note-gen) 创建一个私人仓库。
   - 将克隆的本地文件上传到私人仓库。

3. **公开仓库并启用GitHub Pages**：
   - 将私人仓库设置为公开。
   - 启用GitHub Pages，等待网页构建完成。

4. **修改网页内容**：
   - 使用NoteGen或其他工具修改本地文件。
   - 同步修改后的文件到GitHub，等待网页重新构建。

## 修改网页内容的关键步骤
### 1. 修改个人信息
- **修改`_config.yml`文件**：
  - 修改个人信息，如姓名、职位、学校、联系方式等。
  - 修改`baseurl`为你的GitHub用户名。
  - 确保图片路径正确，例如头像路径应为`/images/your_photo.png`。

- **修改`about.md`文件**：
  - 在`_pages/about.md`中使用Markdown语法添加个人简介。
  - 示例：
    ```markdown
    I'm a third year undergraduate student from [School of EECS](https://eecs.pku.edu.cn/), [Peking University](https://www.pku.edu.cn/). My research interests include computer vision, computer graphics, machine learning, and computational photography.

    You can find my CV here: [Curriculum Vitae](../assets/Curriculum_Vitae.pdf).

    [Email](mailto:your_email@domain.com) / [Github](https://github.com/yourusername) / [Wechat](../images/wechat.jpg)
    ```

### 2. 添加个人照片和文件
- **上传照片**：
  - 将个人照片（如头像）上传到`images`文件夹中，确保文件名与`_config.yml`中的路径一致。
  - 推荐使用PNG格式，避免JPG格式导致的显示问题。

- **上传其他文件**：
  - 将个人简历（如`Curriculum_Vitae.pdf`）上传到`assets`文件夹中。
  - 确保文件路径在`about.md`中正确引用。

### 3. 修改导航栏和页面内容
- **修改导航栏**：
  - 在`_config.yml`文件中修改`header`部分，添加或删除导航栏链接。
  - 示例：
    ```yaml
    header:
      - title: "Home"
        url: /
      - title: "About"
        url: /about/
      - title: "Publications"
        url: /publications/
    ```

- **修改页面内容**：
  - 在`_pages`文件夹中找到对应的页面文件（如`publications.md`），使用Markdown语法修改内容。
  - 示例：
    ```markdown
    ---
    title: "Publications"
    layout: archive
    permalink: /publications/
    ---
    <h2>Selected Publications</h2>
    <ul>
      <li><a href="https://example.com/paper1.pdf">Paper Title 1</a></li>
      <li><a href="https://example.com/paper2.pdf">Paper Title 2</a></li>
    </ul>
    ```

### 4. 使用NoteGen同步修改
- **安装NoteGen**：
  - 下载并安装[NoteGen](https://github.com/codexu/note-gen)。
  - 配置NoteGen以连接到你的私人仓库。

- **修改和同步**：
  - 使用NoteGen修改本地文件（如Markdown文件）。
  - 通过NoteGen同步修改后的文件到GitHub仓库。
  - 等待GitHub Pages重新构建网页。

## 注意事项
- **文件路径**：确保所有文件路径正确无误，避免因路径错误导致文件无法显示。
- **图片格式**：推荐使用PNG格式，避免JPG格式可能导致的显示问题。
- **同步问题**：如果遇到同步问题，可以尝试手动推送更改到GitHub仓库。
- **网页构建**：每次修改后，GitHub Pages需要重新构建网页，可能需要几分钟时间。

## 参考教程
- 详细的修改教程可以参考 [CSDN博客文章](https://blog.csdn.net/qd1813100174/article/details/128604858)，其中提供了完整的修改步骤和示例。