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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438625"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーを順番に閉じます。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in]予約済み。はゼロへのポインターである必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

MAPI は、メッセージ ストア プロバイダー オブジェクトを解放する直前に **IMSProvider::Shutdown** メソッドを呼び出します。 MAPI は、そのプロバイダーの Shutdown を呼び出す前に、プロバイダー **のすべてのログオン** オブジェクトを解放します。 
  
## <a name="see-also"></a>関連項目



[IMSProvider : IUnknown](imsprovideriunknown.md)

