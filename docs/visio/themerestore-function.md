---
title: THEMERESTORE 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: テーマを適用するときに図形のローカル書式の値を格納し、その後でユーザーがテーマを削除した場合にローカル書式を復元できます。
ms.openlocfilehash: 708dcf51a7a01c0f58dab435dd710208b5cb2ff1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597857"
---
# <a name="themerestore-function"></a>THEMERESTORE 関数

テーマを適用するときに図形のローカル書式の値を格納し、その後でユーザーがテーマを削除した場合にローカル書式を復元できます。
  
## <a name="syntax"></a>構文

THEMERESTORE()
  
## <a name="example"></a>例

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

現在のテーマを削除するときに、以前図形に適用された個別の塗りつぶしの色書式を復元します。
  

