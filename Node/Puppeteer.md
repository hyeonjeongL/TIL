<h3> puppeteer </h3>

<br>

- Puppeteer는 Google에서 개발한 Node.js 라이브러리로, Chrome 또는 Chromium 브라우저를 제어하여 웹 페이지를 스크래핑하거나 자동화 테스트를 수행하는 데 사용.
- Puppeteer는 브라우저의 API를 직접 호출하여 브라우저와 상호작용하므로, 사용자가 브라우저에서 수동으로 수행할 수 있는 작업들을 프로그래밍으로 자동화할 수 있음.
- Puppeteer는 웹 페이지를 열고, DOM 요소를 검색하고, 클릭하고, 입력하고, 스크린샷을 캡처하며, 페이지의 콘솔 출력을 가져오는 등 다양한 작업을 수행할 수 있다. 또한, Puppeteer는 Headless 모드에서 작동하며, 이는 브라우저 UI를 표시하지 않고 백그라운드에서 실행되는 모드.
- Puppeteer는 웹 스크래핑과 자동화 테스트 분야에서 인기있는 라이브러리 중 하나이며, 많은 개발자들이 이를 사용하여 웹 애플리케이션을 테스트하고 데이터를 수집.<br><br>

<h3> cheerio </h3>
<br>

- Cheerio는 Node.js에서 사용할 수 있는 HTML 파서 및 조작 라이브러리.
- Puppeteer는 브라우저 기반의 자동화 도구로, 브라우저에서 JavaScript를 실행하며 HTML을 처리할 수 있음.
- Cheerio는 Node.js에서 동작하며, 웹페이지를 가져와서 서버사이드에서 HTML을 처리할 때 유용하게 사용됨.
- Cheerio는 jQuery와 유사한 API를 제공하므로 jQuery를 사용하던 개발자라면 쉽게 사용할 수 있음.
- Puppeteer와 Cheerio는 각각의 특성에 따라 사용 용도가 다름.
<br>
<br>
```
const puppeteer = require('puppeteer');
const cheerio = require('cheerio');

(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.goto('https://example.com');
  const content = await page.content();
  const $ = cheerio.load(content);
  const title = $('h1').text();
  logger.info(title);
  await browser.close();
})();
```

위의 코드는 "https://example.com"사이트의 h1 타이틀을 스크래핑 해오는 코드 
꼭 browser를 마지막에 닫아줘야 한다.
<br>
<br>
<h3>puppeteer와 cheerio의 차이점</h3>
<br>
Puppeteer와 Cheerio는 모두 웹 스크래핑과 자동화 테스트를 위한 도구이지만, 다음과 같은 차이점이 있다.
<br>

- Puppeteer는 브라우저 자동화 도구로, Chrome 또는 Chromium 브라우저를 직접 제어하여 웹 페이지를 스크래핑하거나 자동화 테스트를 수행합니다.
- Cheerio는 Node.js에서 사용할 수 있는 HTML 파서 및 조작 라이브러리로, 브라우저를 사용하지 않고도 HTML 문서를 파싱하고 조작할 수 있습니다.
- Puppeteer는 브라우저에서 실행되는 JavaScript 코드를 실행할 수 있으므로, 브라우저에서 수행할 수 있는 작업들을 자동화할 수 있습니다.
- Cheerio는 Node.js에서 동작하며, HTML 문서를 파싱하고 jQuery와 유사한 API를 제공하여 DOM 요소를 쉽게 선택하고 조작할 수 있습니다.
- Puppeteer는 Headless 모드에서 작동하며, 브라우저 UI를 표시하지 않고 백그라운드에서 실행됩니다.
- Cheerio는 브라우저를 사용하지 않으므로, 백그라운드에서 실행되는 Node.js 애플리케이션에서 HTML 문서를 처리할 수 있습니다.

<br>
따라서 Puppeteer는 브라우저에서 수행하는 작업들을 자동화하기 위한 도구이고, Cheerio는 HTML 문서를 파싱하고 처리하는 데 사용되는 도구입니다. 사용 용도에 따라 두 도구를 적절히 선택하여 사용할 수 있습니다.


