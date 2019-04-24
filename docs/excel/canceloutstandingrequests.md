---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310998"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel Calculation が取り消されたことをクラスター コネクタに通知します。そのため、そのセッションにおいて保留中の関数のすべての呼び出しも取り消される可能性があります (その Excel では、結果を伴うコールバックは必要ありません)。
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>パラメーター

_SessionID_
  
> 取り消された計算で使用されているセッションの ID。この値は、[OpenSession](opensession.md) によって返された値と一致します。
    
## <a name="return-value"></a>戻り値

_SessionId_ 引数が有効な場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、その他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。 
  
## <a name="remarks"></a>注釈

この呼び出し後に受け取る結果はすべて Excel によって破棄されるため、パフォーマンスを向上させるには、実装側でセッションのすべてのプロセスを停止する必要があります。
  
## <a name="see-also"></a>関連項目

- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

