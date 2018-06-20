---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 443644b66ba9c961992e22dbfc260fe8c48fe1b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801503"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**適用されます**: Outlook 
  
オフライン オブジェクトに対してコールバックを登録するのには**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** の情報を提供します。 
  
## <a name="quick-info"></a>クイック ヒント

**IMAPIOfflineMgr::Advise**を参照してください。 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>メンバー

_ulSize_: **MAPIOFFLINE_ADVISEINFO**のサイズです。 
    
_ulClientToken_: コールバックは、クライアントで定義されているトークンです。 *UlClientToken* 、 **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** 構造体のメンバー **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** に渡されたすることをお勧めします。 
    
_CallbackType_: を作成するためのコールバックの種類です。
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - コールバックの種類は、通知されたものです。 これは、コールバックの唯一のサポートされている型です。  *pCallback*は、 **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** インタ フェースを示す必要があります。 
    
_pCallback_: コールバックを使用するインターフェイスです。 これは、 **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** のクライアントの実装です。 
    
_ulAdviseTypes_: のアドバイズ、通知の条件で識別される型。 のみサポートされている型は、MAPIOFFLINE_ADVISE_TYPE_STATECHANGE です。
    
_ulStateMask_: MAPIOFFLINE_STATE_ALL は、唯一サポートされている状態です。
    
## <a name="see-also"></a>関連項目

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [オフラインの状態の API について](about-the-offline-state-api.md) 
- [MAPI �萔](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

