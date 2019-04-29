---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421838"
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

