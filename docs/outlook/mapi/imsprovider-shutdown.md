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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589092"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
適切な順序で、メッセージ ストア プロバイダーを閉じます。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in]予約されています。0 へのポインターである必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

MAPI は、メッセージ ストア プロバイダー オブジェクトを解放する前に、 **IMSProvider::Shutdown**メソッドを呼び出します。 MAPI では、そのプロバイダーの**シャット ダウン**を呼び出す前に、プロバイダーのすべてのログオン オブジェクトを解放します。 
  
## <a name="see-also"></a>関連項目



[IMSProvider : IUnknown](imsprovideriunknown.md)

