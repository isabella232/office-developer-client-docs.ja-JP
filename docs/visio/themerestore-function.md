---
title: THEMERESTORE 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: 場合に復元できるローカルの書式設定、ユーザーが後でテーマを削除するためにテーマを適用するときは、図形のローカル書式設定の値を格納します。
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806655"
---
# <a name="themerestore-function"></a>THEMERESTORE 関数

場合に復元できるローカルの書式設定、ユーザーが後でテーマを削除するためにテーマを適用するときは、図形のローカル書式設定の値を格納します。
  
## <a name="syntax"></a>構文

THEMERESTORE()
  
## <a name="example"></a>例

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

現在のテーマを削除するときに、以前図形に適用された個別の塗りつぶしの色書式を復元します。
  

