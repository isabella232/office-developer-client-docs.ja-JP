---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409784"
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

