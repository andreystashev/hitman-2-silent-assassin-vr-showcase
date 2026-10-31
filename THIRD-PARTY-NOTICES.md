# Third-party notices

Hitman 2: Silent Assassin is a game by IO Interactive. Names and trademarks belong to their respective owners. This independent community mod does not include or license the original game.

Bundled components retain their own terms. Their licenses do not grant an overall source-code license for the mod.

| Component | Use | License/notice |
| --- | --- | --- |
| MinHook, including Hacker Disassembler Engine | Native function hooks | [MinHook license](licenses/MinHook-LICENSE.txt) |
| Oculus PC SDK / LibOVR headers | Interface to installed Meta PC runtime | [Oculus SDK license](licenses/Oculus-SDK-LICENSE.txt) |
| OpenXR SDK | Bundled x64 Khronos loader and interface headers | [OpenXR Apache-2.0 license](licenses/OpenXR-LICENSE.txt) |
| JsonCpp | JSON support inside the OpenXR loader | [JsonCpp public-domain/MIT license](licenses/JsonCpp-LICENSE.txt) |
| DXVK 3.1.1 | Bundled x86 D3D8/D3D9 Vulkan wrappers | [DXVK license](licenses/DXVK-LICENSE.txt) |
| d3d8to9 | Optional D3D8 to Microsoft D3D9On12 renderer | [BSD-2-Clause license](licenses/d3d8to9-LICENSE.txt) |
| LLVM / Clang | Compiler/runtime notices | [LLVM license](licenses/LLVM-LICENSE.txt) |
| libc++ | Statically linked C++ library | [libc++ license](licenses/libcxx-LICENSE.txt) |
| libc++abi | Statically linked C++ ABI runtime | [libc++abi license](licenses/libcxxabi-LICENSE.txt) |
| libunwind | Exception-unwinding runtime | [libunwind license](licenses/libunwind-LICENSE.txt) |
| compiler-rt | Compiler support runtime | [compiler-rt license](licenses/compiler-rt-LICENSE.txt) |
| MinGW-w64 runtime | Windows startup/runtime support | [Runtime notices](licenses/MinGW-w64-runtime-LICENSE.txt) |
| winpthreads | Windows threading support | [winpthreads notices](licenses/winpthreads-LICENSE.txt) |
| EarTrumpet reference | Windows per-application audio-policy interface reference | [Audio interface notice](licenses/THIRD-PARTY-AUDIO.txt) |

The Meta, SteamVR and Virtual Desktop headset runtimes are loaded from the user's installed PC VR software and are not bundled. The OpenXR loader is not a headset runtime. The Oculus SDK remains subject to its own terms, including its approved-platform provisions.

No EarTrumpet application, service or executable is included. The audio interface reference notice is supplied in full with the release.

The optional recorder uses separately installed Python, FFmpeg and Python packages. These are not part of the installer.

Upstream projects: [MinHook](https://github.com/TsudaKageyu/minhook), [OpenXR SDK](https://github.com/KhronosGroup/OpenXR-SDK), [DXVK](https://github.com/doitsujin/dxvk/releases/tag/v3.1.1), [EarTrumpet](https://github.com/File-New-Project/EarTrumpet).

Microsoft D3D9On12 and the D3DX9_43 prerequisite are loaded from the installed Windows/DirectX environment, not redistributed as Microsoft runtime binaries in this mod. The modified d3d8to9 translator retains its upstream BSD-2-Clause notice.
