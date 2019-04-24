---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304138"
---
# <a name="closesession"></a>CloseSession

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
クラスターでセッションを終了します。
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>パラメーター

_SessionId_
  
> 閉じるセッションの ID。この値は、[OpenSession](opensession.md) で返された値に一致する必要があります。
    
## <a name="return-value"></a>戻り値

セッションが閉じられた場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、その他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。 
  
## <a name="see-also"></a>関連項目

- [OpenSession](opensession.md)
- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

