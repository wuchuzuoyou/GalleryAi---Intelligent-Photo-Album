# GalleryAI

**隐私优先的 Android 相册。**&#8203; 谷歌相册式的照片流，加上一套完整跑在设备上的
AI 构图与影调工作流——所有模型都在本机推理，照片不出设备；云端视觉大模型是可选增强，
默认关闭，仓库不含任何凭据。

- **看得舒服**：justified 拼贴网格（3.4 密度）、捏合切挡、FastScroller 快滚、液态玻璃底栏；
  查看器支持 Ultra HDR / XDR 增益图与分层解码，大图不 OOM。
- **拍得更好**：YOLO11n-pose 判断姿态与视线、GAICv2 整图美学初筛、NIMA 打分、
  U²-Net 分割主体、ML Kit 找人脸，再交给构图规则轴与硬约束漏斗产出候选裁切。
  24 张基准图在小米 14 Ultra 上热态 P50 约 2.0 s。
- **调得准**：33³ 3D LUT 三线性采样（零分配）、`.cube` 导入、CIEDE2000 肤色安全校准；
  AI 只做推荐，渲染与导出走自研管线——JPEG q98 baseline、EXIF 继承、HDR gainmap 保留。

技术栈：Kotlin + Jetpack Compose + Hilt + Room + Paging3 + ONNX Runtime（CPU EP），
RAW 走 libraw NDK，仅 arm64-v8a，Android 14（API 34）起。当前 `4.10.2` / `vc201`，MIT。

## 捐赠

捐赠完全自愿。**是否捐赠不会影响项目的功能、下载、更新、使用权限或问题反馈，任何功能均不会以捐赠为前提。**

收到的捐赠将全部用于购买 Token，以支持后续开发、调试和验证。捐赠不构成购买行为，也不附带功能、进度、支持优先级或其他回报承诺。

<img width="1260" height="1890" alt="1788187629390" src="https://github.com/user-attachments/assets/674f8f2f-c9a1-4d00-be90-caef6537ded5" />
