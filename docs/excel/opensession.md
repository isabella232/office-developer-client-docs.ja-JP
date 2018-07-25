---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798938"
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

