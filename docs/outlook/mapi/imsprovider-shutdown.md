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
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801052"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**適用されます**: Outlook 
  
適切な順序で、メッセージ ストア プロバイダーを閉じます。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in]予約されています。0 へのポインターである必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>備考

MAPI は、メッセージ ストア プロバイダー オブジェクトを解放する前に、 **IMSProvider::Shutdown**メソッドを呼び出します。 MAPI では、そのプロバイダーの**シャット ダウン**を呼び出す前に、プロバイダーのすべてのログオン オブジェクトを解放します。 
  
## <a name="see-also"></a>関連項目



[IMSProvider: IUnknown](imsprovideriunknown.md)

