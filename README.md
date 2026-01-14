# 388D_Test1_Workspace

이 저장소의 F28388D 예제를 위한 TI C2000 CCS 워크스페이스입니다.

## 프로젝트
- `adc_ex1_epwm_input` (CPU1)
- `adc_ex1_epwm_input_cpu2` (CPU2)

## 레이아웃
각 프로젝트의 소스는 `core/` 아래에 위치합니다.
- `core/c` : C 소스
- `core/cc` : C++ 소스
- `core/asm` : 어셈블리

링커 커맨드 파일(`*.cmd`)은 프로젝트 루트에 둡니다.

## 빌드 (CCS)
1. Code Composer Studio 20.4.0 이상 설치 (ccs2040 레이아웃 기준).
2. C2000Ware 설치 (`C2000Ware_6_00_01_00` 기준).
3. TI CGT C2000 컴파일러 v22.6.3 LTS 이상 사용.
4. CCS 워크스페이스에 두 프로젝트를 Import.
5. 원하는 구성으로 빌드 (`CPU1_RAM`, `CPU2_RAM` 등).

이 워크스페이스에서 사용하는 기본 설치 경로:
- CCS: `/opt/ti/ccs2040`
- C2000Ware: `/opt/ti/c2000/C2000Ware_6_00_01_00`
- TI CGT C2000 컴파일러: `/opt/ti/ccs2040/ccs/tools/compiler/ti-cgt-c2000_22.6.3.LTS/bin/cl2000`

## IntelliSense/clangd
CCS는 빌드 후 `CPU*_RAM/.clangd/` 아래에 `compile_commands.json`을 생성합니다. 에디터에서 해당 파일을 지정하면 include 경로와 define을 올바르게 인식합니다.
