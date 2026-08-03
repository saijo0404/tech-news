# NVIDIA Video Codec SDK 13.1: Zero-Copy Transcode, AV1 B-Frames, and Frame-Accurate Seek

- **來源**: NVIDIA Developer Blog
- **發布日期**: 2026-07-31
- **原文連結**: https://developer.nvidia.com/blog/nvidia-video-codec-sdk-13-1-zero-copy-transcode-av1-b-frames-and-frame-accurate-seek/

## 核心主題
NVIDIA Video Codec SDK 13.1 推出多项视频编解码改进，包括 AV1 分层参考模式、零拷贝转码和精确帧搜索功能，显著提升视频处理效率与质量。

## 關鍵重點
- **AV1 分层参考模式**：支持最多 31 个 B-frames，提升编码质量与效率，无额外性能负担
- **解码改进**：提供每宏块统计信息（QP、编码单元类型、运动向量）及 GOP-aware 精确帧搜索功能
- **转码器重新设计**：采用模块化队列架构，支持零拷贝转码，降低内存带宽使用并提升吞吐量
- **MV-HEVC 立体影像支持**：支持 view/layer metadata 及第三方相容性，优化 3D/XR 视频处理
- **Docker 开发环境**：官方 Docker 基开发环境，将 CUDA、Vulkan、FFmpeg 统一打包，解决环境配置问题

## 結論
SDK 13.1 通过多项关键改进，为开发者提供了更强大的视频处理工具链，特别适用于 AI 工作流、高解析度 3D/XR 视频处理以及需要精确帧访问的场景。零拷贝转码和精确帧搜索功能将显著提升视频处理系统的性能与灵活性。

---