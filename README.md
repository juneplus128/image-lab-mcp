# Image Lab MCP — 학생용 다운로드

[학생용 ZIP 다운로드](https://github.com/mark00425-sys/image-lab-mcp/releases/download/v0.5.0/Image-Lab-Student-Pack-0.5.0.zip)

ZIP 하나에 MCPB 설치 파일, 90×90 샘플 이미지, Image-Lab-Images 폴더, output 폴더, 설치 안내가 포함되어 있습니다.

## 설치

1. 위 ZIP을 다운로드하고 압축을 해제하세요.
2. Claude Desktop에서 Image-Lab-MCP-0.5.0.mcpb를 열어 설치하세요.
3. 확장프로그램 설정의 이미지 폴더로 ZIP 안의 Image-Lab-Images 폴더를 선택하세요.
4. 새 대화에서 아래 프롬프트를 입력하세요.

> Image Lab으로 test-image-90x90.png를 backend=ai로 4배 업스케일하고 결과 이미지를 보여줘.

내 이미지를 사용하려면:

> Image Lab의 pick_image로 파일 선택 창을 열어줘. 내가 선택한 이미지를 backend=ai로 4배 업스케일하고 결과 이미지를 보여줘.

## 동작

Clark Swin2SR 경량 2× 모델을 포함합니다. AI 2배는 1회, AI 4배는 2회 실행합니다. Node.js/Python을 별도로 설치하지 않아도 됩니다. Claude Desktop은 별도로 필요합니다.

결과 전체 PNG는 Image-Lab-Images/output에 저장됩니다. 최대 1024픽셀 미리보기를 MCP 이미지 응답으로 반환하며, 실제 대화 표시 여부는 Claude 클라이언트 지원에 달려 있습니다. 처리는 로컬이지만 미리보기는 Claude에 전달됩니다.

Claude 채팅 첨부 이미지 자동 전달은 지원하지 않습니다. 파일 선택 창을 사용하세요. CPU에서 큰 이미지는 오래 걸릴 수 있으며 AI 제한시간은 120초입니다. backend=ai는 실패 시 오류를 반환하고 auto는 일반 보간으로 전환할 수 있습니다.

Windows/macOS용입니다. Windows 실제 설치 및 네이티브 파일 선택 창 검증은 아직 완료되지 않았습니다.

모델 출처와 라이선스는 ZIP 및 MCPB 안에 포함되어 있습니다.
