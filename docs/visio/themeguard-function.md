---
title: THEMEGUARD 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: 図形の書式設定セルを保護して、現在のテーマの適切な側面を使用します。
ms.openlocfilehash: e29fdd9c148940e047a7f97a8e6d5b72d685f7cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603348"
---
# <a name="themeguard-function"></a>THEMEGUARD 関数

図形の書式設定セルを保護して、現在のテーマの適切な側面を使用します。
  
## <a name="syntax"></a>構文

THEMEGUARD()
  
## <a name="remarks"></a>注釈

THEMEGUARD 関数をセルに適用しても、GUARD 関数の場合と同様、手動でフォーマットを適用することは可能です。 ユーザー インターフェイスの図形に書式を適用するか、オートメーションを使用してプログラムによって書式設定を適用すると、手動書式の値を格納する数式に SETATREFEXPR 関数を含めない限り、THEMEGUARD 数式はオーバーライドされます。 
  
## <a name="example"></a>例

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

主テーマに設定された塗りつぶし色の代わりに、現在のテーマの Accent 2 の色で図形を塗りつぶすよう指定します。
  

