## 관련 모듈
- request: 페이지 요청
- iconv: 인코딩 변환
- jsdom: 돔 탐색

## 유의 사항
1. 인코딩 변환이 필요한 경우 request options에 encoding을 'binary'로 설정해서 불러온다
```javascript
let options = {
  url: url,
  encoding: 'binary'
};
```

2. 인코딩 변환 시점은 request로 불러오자마자 시도한다
```javascript
request(options, (req, res, body) => {
  let bodyBuffer = new Buffer(body, 'binary');
  let text = iconv.convert(bodyBuffer).tostring();
});
```

3. 기계수집을 막아놓은 사이트인 경우 headers - User Agent에 약간의 속임수를 준다
```javascript
{
  headers: {
    'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10.11; rv:43.0) Gecko/20100101 Firefox/43.0'
  }
}
```