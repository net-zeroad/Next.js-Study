# Next.js-Study
- 인프런 강좌 학습
  - 타입스크립트 코리아(React with TypeScript 세미나) : https://www.inflearn.com/course/react-with-typescript/dashboard


# 기본 설치방법
- yarn 설치
```yarn init -y```
- next/react/react-dom 라이브러리 설치
```yarn add next react react-dom```


# Next.js 라이브러리 기본 사용방법
1. 생성된 package.json에 scripts 추가

"scripts": {
    "dev": "next",
    "build": "next build",
    "start": "next start"
  },

2. pages 폴더 생성(라우터가 될 파일을 내부에 작성해준다.)
- 기본 root 컴포넌트가 될 index.js 파일 생성하여 내부에 컴포넌트 함수 생성 및 export
```
export default () => {
    return (
        <>
            <h2>Happy World !</h2>
        </>
    );
}
```


# 기본 실행방법
- 3000 port server 실행(pages 없으면 실행되지 않는다.)
```yarn next```
 

# Next.js의 라우터 설정방법
- Links.js 컴포넌트(src에 components 폴더 만든 후 내부에 생성)
  - 라이브러리 가져옴
```import Link from 'next/link';```
  - 이동할 링크 설정(a태그와 같다) 및 export 해준다.
```
export default () => {
    return (
        <ul>
            <li><Link href={"/"}>root</Link></li>
            <li><Link href={"/happy"}>happy</Link></li>
        </ul>
    );
}
```
 
- 라우터를 설정해보기 위해 /happy 라우터가 될 happy.js 파일 생성
  - 생성한 컴포넌트 불러오기
```import Links from "../components/Links";```


- Links 컴포넌트가 import 되었다면 index.js, happy.js 등의 컴포넌트에서 아래와 같이 Link 컴포넌트를 불러올 수 있다.
```
export default () => {
    return (
        <>
            <h2>해피컴포넌트</h2>
            <Links />
        </>
    );
}
```
 

 
