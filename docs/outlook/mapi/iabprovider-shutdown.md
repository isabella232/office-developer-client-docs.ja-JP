---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ba11186c21562b14ff61d7128d9cf70028bb2201
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584480"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アクティブなセッションへの接続をキャンセルします。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [In]予約済み。はゼロへのポインターである必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 接続が正常に取り消されました。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**Shutdown** メソッドの実装では、必要と思うタスクを実行します。 MAPI は、 **すべてのログオン** オブジェクトを解放した後にのみ、Shutdown メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IABProvider : IUnknown](iabprovideriunknown.md)

