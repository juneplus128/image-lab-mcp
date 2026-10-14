# Image Lab MCP — 학생용 다운로드

[학생용 ZIP 다운로드 · 0.6.0](https://github.com/mark00425-sys/image-lab-mcp/releases/download/v0.6.0/Image-Lab-Student-Pack-0.6.0.zip)

**리모트 MCP 연결 주소 — 복사해서 사용하세요**

```text
https://image-upscaler-mcp.image-upscaler-mcp.workers.dev/mcp
```

주소를 드래그해서 복사하거나 코드 블록 오른쪽 위 복사 버튼을 누르세요. 복사한 주소를 리모트 MCP 연결 설정에 붙여 넣으세요.

ZIP 하나에 MCPB 설치 파일, 90×90 샘플 이미지, Image-Lab-Images/output 폴더, 설치 안내가 포함되어 있습니다.

## 설치 및 업데이트

1. 위 ZIP을 다운로드하고 압축을 해제하세요.
2. Claude Desktop에서 Image-Lab-MCP-0.6.0.mcpb를 열어 설치하거나 기존 확장을 업데이트하세요.
3. 설정의 이미지 폴더로 ZIP 안의 Image-Lab-Images 폴더를 선택하세요.
4. 새 대화에서 아래 프롬프트를 입력하세요.

> Image Lab의 pick_image로 파일 선택 창을 열어줘. 내가 선택한 이미지를 AI로 4배 업스케일하고 확대 전후 비교 화면을 열어줘. backend는 ai, show_comparison은 true로 실행해줘.

샘플 테스트:

> Image Lab으로 test-image-90x90.png를 backend=ai, show_comparison=true로 4배 업스케일하고 확대 전후 비교 화면을 열어줘.

## 확대 전후 비교

0.6.0부터 처리가 끝나면 기본 브라우저에 원본과 결과가 나란히 표시되는 로컬 비교 화면이 열립니다. 최대1600픽셀 미리보기이며 전체 해상도 PNG는 output 폴더에 저장됩니다. 자동으로 열리지 않으면 도구 응답의 comparison_path HTML을 직접 열어주세요.

## 동작

Clark Swin2SR 경량 2× 모델: AI 2배는 1회, AI 4배는 2회 실행합니다. Node.js/Python 별도 설치는 필요하지 않으며 Claude Desktop은 별도로 필요합니다.

처리는 로컬입니다. 비교 HTML은 이미지를 포함하며 외부 서버에 접속하지 않습니다. MCP 미리보기 이미지는 Claude에 전달됩니다. Claude 대화창 표시 여부는 클라이언트 지원에 달려 있습니다.

Claude 채팅 첨부 이미지의 자동 전달은 지원하지 않습니다. pick_image 파일 선택 창을 사용하세요. CPU에서 큰 이미지는 오래 걸릴 수 있고 AI 제한시간은 120초입니다. backend=ai는 실패 시 오류를 반환하며 auto는 일반 보간으로 전환할 수 있습니다.

Windows/macOS용입니다. Windows 실제 설치, 파일 선택 창 및 자동 브라우저 열기 검증은 미완료입니다. 모델 출처와 라이선스는 ZIP과 MCPB에 포함되어 있습니다.

로컬 MCPB 0.6.0 업데이트이며 리모트 MCP 서버의 기능은 별도로 운영됩니다.
