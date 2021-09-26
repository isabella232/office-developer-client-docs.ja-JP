---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a9103430bf340837f22302d5ba76adcb197e8fdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631497"
---
# <a name="opensession"></a>OpenSession

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザー定義関数を実行できるセッションを作成します。
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>パラメーター

_Params_
  
> セッションのパラメーターの、セミコロンで区切られた UNICODE 文字列へのポインター。Excel では、この引数は使用しません。
    
## <a name="return-value"></a>戻り値

セッションが正常に作成された場合は、このクラスター コネクタに対する他の呼び出しで使用するセッション ID。それ以外の場合は **xlHpcRetCallFailed**。
  
## <a name="see-also"></a>関連項目

- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

