---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 195feaebe15d6306859d8b5112f4fb2f05134ff9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621389"
---
# <a name="pingsession"></a>PingSession

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
セッションが有効かどうかをチェックします。この関数は通常、以前返されたセッション ID が現在もアクティブで使用可能かどうかを Excel で判断する必要がある場合に呼び出されます。
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>パラメーター

_SessionID_
  
> ping を実行するセッションの ID。この値は、前回 [OpenSession](opensession.md) を呼び出した際に返された ID と一致する必要があります。
    
## <a name="return-value"></a>戻り値

_SessionId_ 引数が有効な場合は **xlHpcRetSuccess** を返します。それ以外の場合は **xlHpcRetInvalidSessionId** を返します。
  
## <a name="see-also"></a>関連項目

- [OpenSession](opensession.md)
- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

