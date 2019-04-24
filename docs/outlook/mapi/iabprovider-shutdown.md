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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348903"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アクティブなセッションへの接続を取り消します。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lアウトフラグ_
  
> 順番予約語0へのポインターである必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 接続が正常にキャンセルされました。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**シャットダウン**方法の実装で、必要と考えられるすべてのタスクを実行します。 MAPI は、すべてのログオンオブジェクトを解放した後にのみ、 **Shutdown**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IABProvider : IUnknown](iabprovideriunknown.md)

