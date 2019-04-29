---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420025"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[IMAPIOfflineMgr::](imapiofflinemgr-advise.md)** 通知して、オフラインオブジェクトのコールバックを登録するようにアドバイスします。 
  
## <a name="quick-info"></a>クイック ヒント

「 **IMAPIOfflineMgr:: Advise**」を参照してください。 
  
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

_ulsize_: **MAPIOFFLINE_ADVISEINFO**のサイズ。 
    
_ulclienttoken_: クライアントによってコールバックに対して定義されたトークン。 これは、 **[IMAPIOfflineNotify:: NOTIFY](imapiofflinenotify-notify.md)** に渡される**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** 構造の*ulclienttoken*メンバーです。 
    
/_テキスト_: 作成するコールバックの種類。
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - コールバックの種類は、通知によって行います。 これは、サポートされている唯一の種類のコールバックです。  *pcallback*は、インターフェイス**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を示す必要があります。 
    
_pcallback_: コールバックに使用するインターフェイス。 これは、クライアントによる**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** の実装です。 
    
_ulAdviseTypes_: アドバイスの条件で識別される、アドバイスの種類。 サポートされている唯一の種類は MAPIOFFLINE_ADVISE_TYPE_STATECHANGE です。
    
_ulStateMask_: サポートされている唯一の状態は、MAPIOFFLINE_STATE_ALL です。
    
## <a name="see-also"></a>関連項目

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [オフライン状態 API について](about-the-offline-state-api.md) 
- [MAPI �萔](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

