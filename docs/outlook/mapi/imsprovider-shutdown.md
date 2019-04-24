---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317263"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーを整然と閉じます。
  
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
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

MAPI は、メッセージストアプロバイダオブジェクトを解放する直前に、 **IMSProvider:: Shutdown**メソッドを呼び出します。 MAPI は、そのプロバイダーの**シャットダウン**を呼び出す前に、プロバイダーのすべてのログオンオブジェクトを解放します。 
  
## <a name="see-also"></a>関連項目



[IMSProvider : IUnknown](imsprovideriunknown.md)

