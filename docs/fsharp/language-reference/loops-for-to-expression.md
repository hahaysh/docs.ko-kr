---
title: '루프: for...to 식(F#)'
description: '참조 하는 방법을 F # 하십시오... 식으로 루프 변수 값의 범위에 대해 루프를 반복에 사용 됩니다.'
ms.date: 05/16/2016
ms.openlocfilehash: 8160fd30c4f3afe8bb6b58f468802ef1c0ef32ee
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43800471"
---
# <a name="loops-forto-expression"></a>루프: for...to 식

`for...to` 식은 루프 변수 값의 범위에 대해 루프를 반복 하는 데 사용 됩니다.

## <a name="syntax"></a>구문

```fsharp
for identifier = start [ to | downto ] finish do
    body-expression
```

## <a name="remarks"></a>설명

식별자의 형식은 형식에서 유추 됩니다 합니다 *시작* 하 고 *마침* 식입니다. 이러한 식에 대 한 형식에는 32 비트 정수 여야 합니다.

하지만 식을 기술적 `for...to` 명령형 프로그래밍 언어에서 일반적인 문에 같습니다. 반환 형식은 합니다 *식 본문* 이어야 합니다 `unit`합니다. 다음 예제에서는 표시의 다양 한 용도 `for...to` 식입니다.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5101.fs)]

위 코드는 다음과 같이 출력됩니다.

```
1 2 3 4 5 6 7 8 9 10
10 9 8 7 6 5 4 3 2 1
2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18
```

## <a name="see-also"></a>참고자료

- [F# 언어 참조](index.md)
- [루프: `for...in` 식](loops-for-in-expression.md)
- [루프: `while...do` 식](loops-while-do-expression.md)
