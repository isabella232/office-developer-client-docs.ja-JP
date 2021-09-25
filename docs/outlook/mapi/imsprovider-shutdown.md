---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 79137939ef6f40704804e5a3499c36cc2271c7fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630531"
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

