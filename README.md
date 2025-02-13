# Ocean Breeze 정신 건강 체크

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 소개 (Introduction)

Ocean Breeze 정신 건강 체크는 PHQ-9 (Patient Health Questionnaire-9) 설문을 기반으로 제작된 웹 애플리케이션입니다. 사용자의 정신 건강 상태, 특히 우울 증상의 정도를 간략하게 평가하는 데 도움을 줍니다. 이 도구는 자가 진단을 위한 것이며, 전문적인 의학적 진단이나 치료를 대체할 수 없습니다.

## 주요 특징 (Features)

*   **PHQ-9 기반:** 신뢰할 수 있는 PHQ-9 설문 문항을 사용합니다.
*   **반응형 디자인:** 모바일, 태블릿, 데스크톱 등 다양한 기기에서 최적화된 사용자 경험을 제공합니다.
*   **아이폰 최적화:** 아이폰 Safari 브라우저에서의 렌더링 및 터치 인터랙션을 고려하여 설계되었습니다.
*   **PWA (Progressive Web App):** "홈 화면에 추가" 기능을 통해 네이티브 앱처럼 사용할 수 있습니다. (아이콘 제공 필요)
*   **부드러운 애니메이션:** CSS transitions와 animations를 사용하여 사용자 인터페이스를 개선했습니다.
*   **접근성 (Accessibility):** 웹 접근성 표준을 준수하여 다양한 사용자가 이용할 수 있도록 했습니다. (WAI-ARIA 속성 활용 등)
*   **직관적인 UI:** 깔끔하고 사용하기 쉬운 인터페이스를 제공합니다.
*   **결과 제공:** 우울 증상의 정도를 백분율(%)로 표시하고, 그에 따른 간단한 해석을 제공합니다.
*   **개인 정보 보호:** 사용자 데이터를 서버에 저장하지 않습니다. 모든 데이터는 브라우저 내에서 처리됩니다.
*   **이전/다음 버튼:** 모바일 사용성을 위한 질문 간 이동 버튼을 제공합니다.

## 기술 스택 (Tech Stack)

*   **HTML5:** 시맨틱 마크업을 사용하여 구조를 정의했습니다.
*   **CSS3:** 반응형 디자인, 애니메이션, 테마를 적용했습니다.
*   **JavaScript (ES6+):** 사용자 상호작용, PHQ-9 점수 계산, 결과 표시 로직을 처리합니다.
*   **Google Fonts (Noto Sans KR):** 가독성이 좋은 한국어 폰트를 사용했습니다.

## 설치 및 사용 방법 (Installation and Usage)

1.  **코드 다운로드:** 이 저장소(repository)를 클론(clone)하거나 ZIP 파일로 다운로드합니다.
    ```bash
    git clone <repository_url>
    ```
2.  **HTML 파일 열기:** `index.html` 파일을 웹 브라우저(Chrome, Safari, Firefox 등)에서 엽니다.  별도의 서버 설정 없이 바로 사용할 수 있습니다.
3.  **아이콘 생성 (PWA):** `icon-180x180.png` (아이폰용) 및 `favicon.png` (기타 브라우저용) 파일을 생성하여 루트 디렉토리에 추가합니다. 다양한 크기의 아이콘을 생성하여 `/images/icons/` 디렉터리를 만들고 `manifest.json` 파일에 추가하면 더 완벽한 PWA 지원이 됩니다.
4. **(선택 사항) 웹 서버 배포:** 더 많은 사용자와 공유하려면, 웹 서버(Apache, Nginx, Netlify, GitHub Pages 등)에 배포할 수 있습니다.

## PWA 설정 (Optional - for a full PWA experience)

1.  **manifest.json 생성:** 아래 내용과 같이 `manifest.json` 파일을 생성하여 루트 디렉토리에 추가합니다.

    ```json
    {
      "name": "Ocean Breeze 정신 건강 체크",
      "short_name": "Ocean Breeze",
      "description": "PHQ-9 기반 정신 건강 자가 진단 도구",
      "start_url": "/",
      "display": "standalone",
      "background_color": "#ffffff",
      "theme_color": "#3498db",
      "icons": [
        {
          "src": "images/icons/icon-72x72.png",
          "sizes": "72x72",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-96x96.png",
          "sizes": "96x96",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-128x128.png",
          "sizes": "128x128",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-144x144.png",
          "sizes": "144x144",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-152x152.png",
          "sizes": "152x152",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-192x192.png",
          "sizes": "192x192",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-384x384.png",
          "sizes": "384x384",
          "type": "image/png"
        },
        {
          "src": "images/icons/icon-512x512.png",
          "sizes": "512x512",
          "type": "image/png"
        }
      ]
    }

    ```
    *   `images/icons/` 디렉터리를 만들고, 다양한 크기의 아이콘들을 생성하여 추가합니다. (72x72, 96x96, 128x128, 144x144, 152x152, 192x192, 384x384, 512x512).
    *  필요에 따라 `name`, `short_name`, `description`, `start_url`, `background_color`, `theme_color` 값을 수정합니다.

2.  **manifest.json 링크:** `index.html` 파일의 `<head>` 섹션에 다음 코드를 추가합니다.

    ```html
    <link rel="manifest" href="manifest.json">
    ```

3. **Service Worker 등록 (Optional - Offline Support):** 오프라인 지원을 위해서는 Service Worker를 등록해야 합니다. 이는 고급 기능이며, 이 README에서는 다루지 않습니다.  필요한 경우, Workbox와 같은 라이브러리를 사용하여 Service Worker를 쉽게 생성할 수 있습니다.

## 기여 (Contributing)

버그를 발견하거나 개선 제안이 있으면, GitHub Issues에 이슈를 등록하거나 Pull Request를 보내주세요. 기여는 언제나 환영합니다!

## 라이선스 (License)

이 프로젝트는 MIT 라이선스에 따라 배포됩니다. 자세한 내용은 `LICENSE` 파일을 참조하세요.
