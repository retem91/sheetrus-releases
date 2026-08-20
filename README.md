# Sheetrus Releases

Sheetrus **배포 전용** public 저장소입니다. 소스 코드는 포함하지 않습니다.

| 저장소 | 용도 |
|--------|------|
| [sheetrus-flutter](https://github.com/retem91/sheetrus-flutter) (private) | Flutter 앱 소스 |
| [sheetcastle-electron](https://github.com/retem91/sheetcastle-electron) (private) | Electron 앱 소스 |
| **sheetrus-releases** (public) | APK, 설치 파일, 업데이트 manifest |

## 릴리즈 태그 규칙

| 플랫폼 | 태그 예 | asset |
|--------|---------|-------|
| Android op | `android-v1.2.0` | `app-op-release.apk`, `update-manifest.json` |
| Electron (예정) | `electron-v1.2.0` | `Sheetrus-Setup-x.y.z.exe`, `latest.yml` |

Flutter 앱은 `update-manifest.json`이 포함된 **가장 최신 Android 릴리즈**를 조회합니다.

## Android 배포 (CI)

`sheetrus-flutter`에 `v*` 태그를 push하면 GitHub Actions가 APK를 빌드해 이 저장소에 업로드합니다.

필수 Secret (`sheetrus-flutter` → Settings → Secrets):

- `GH_RELEASE_TOKEN` — 이 저장소에 `contents: write` 권한이 있는 PAT
- `RELEASE_*` — Android keystore
- `OP_SUPABASE_*` — 운영 env

## 다운로드

https://github.com/retem91/sheetrus-releases/releases
