# TeeTools — Avatar Health Check

🇯🇵 [日本語 README はこちら](README.ja.md)

Scans a VRChat avatar for common performance and upload issues and gives a
beginner-friendly report: what was found, whether it's actually worth
worrying about, and what to do next.

First tool in the TeeTools series for VRChat avatar creators.

## Install (via VCC)

1. Add the TeeTools repository to VCC (see the main repo's README/index for
   the current "Add to VCC" link).
2. Open your avatar project in VCC.
3. Find "TeeTools - Avatar Health Check" under Packages and click Add.

## Use

`TeeTools > Avatar Health` in Unity's menu bar. Drag your avatar's root
GameObject into the Target Avatar field and click Scan.

The tool itself has an in-app language switch (English / 日本語) in the
top-right corner of its window — this README is just for setup instructions.

## Notes

- No dependency on the VRChat SDK is declared, since PhysBone/PhysBone
  Collider/VRCAvatarDescriptor checks are done via reflection — the tool
  installs and runs fine even in a project without the SDK yet, it just
  skips those specific checks and says so.
- Thresholds (poly count, material count, texture size, etc.) are rule-of-thumb
  values in `HealthCheckConfig` inside `AvatarHealthCheck.cs` — adjust freely.
