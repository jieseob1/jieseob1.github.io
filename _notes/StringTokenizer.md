---
title: "StringTokenizer 사용법"
dg-publish: true
date: 2024-10-02
tags: [java, algorithm]
---
### 개요
- overload되어서 각각 어떤 기능들이고, 각 기능들에 따른 메소드는 어떤 기능들을 하는지에 대해서 궁금함


## **생성자**

1. **`StringTokenizer(String str)`**:
    
    - 이 생성자는 기본 구분자를 사용하여 지정된 문자열에 대한 `StringTokenizer`를 생성합니다. 기본 구분자는 공백 문자(예: 스페이스, 탭, 줄바꿈 등)입니다.
    
2. **`StringTokenizer(String str, String delim)`**:
    
    - 이 생성자는 구분자 집합을 지정할 수 있습니다. `delim` 문자열의 각 문자는 유효한 구분자로 간주됩니다.
    
3. **`StringTokenizer(String str, String delim, boolean returnDelims)`**:
    
    - 이 생성자는 이전 것과 비슷하지만, `returnDelims`라는 불리언 플래그를 포함합니다. `true`로 설정하면 구분자 자체도 토큰으로 반환됩니다. `false`로 설정하면 구분자는 토큰을 분리하는 데만 사용되고 반환되지 않습니다.


## **메서드**

- **`int countTokens()`**:
    
    - 문자열에 남아 있는 토큰의 수를 반환합니다. 이 메서드는 `nextToken()` 메서드를 호출할 수 있는 횟수를 계산합니다.
    
- **`boolean hasMoreTokens()`**:
    
    - 문자열 토크나이저에 더 많은 토큰이 있는지 확인합니다. 더 많은 토큰이 있으면 `true`, 그렇지 않으면 `false`를 반환합니다.
    
- **`String nextToken()`**:
    
    - 문자열 토크나이저에서 다음 토큰을 반환합니다. 더 이상 토큰이 없으면 `NoSuchElementException`을 발생시킵니다.
    
- **`String nextToken(String delim)`**:
    
    - 다음 토큰을 검색할 때 새로운 구분자 집합을 지정할 수 있는 오버로드된 버전입니다.
    
- **`boolean hasMoreElements()`**:
    
    - `hasMoreTokens()`와 동일한 값을 반환하며, `StringTokenizer`가 `Enumeration` 인터페이스를 구현하기 때문에 포함되었습니다.
    
- **`Object nextElement()`**:
    
    - `nextToken()`과 유사하지만 `String` 대신 `Object`를 반환합니다. 이것도 `Enumeration` 인터페이스 구현 때문입니다.