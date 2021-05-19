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
# <a name="mapioffline_adviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[IMAPIOfflineMgr::Advise に](imapiofflinemgr-advise.md)** オフライン オブジェクトのコールバックを登録するための情報を提供します。 
  
## <a name="quick-info"></a>クイック ヒント

**「IMAPIOfflineMgr::Advise」を参照してください**。 
  
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

## <a name="members"></a>Members

_ulSize_: サイズ **は** MAPIOFFLINE_ADVISEINFO です。 
    
_ulClientToken_: コールバックに関するクライアントによって定義されたトークン。 *IMAPIOfflineNotify::Notify* **[](mapioffline_notify.md)** に渡MAPIOFFLINE_NOTIFY構造の **[ulClientToken メンバーです](imapiofflinenotify-notify.md)**。 
    
_CallbackType_: 作成するコールバックの種類。
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - コールバックの種類は通知別です。 これは、サポートされているコールバックの唯一の種類です。  *pCallback は*  、インターフェイス **[IMAPIOfflineNotify を示す必要があります](imapiofflinenotifyiunknown.md)**。 
    
_pCallback_: コールバックに使用するインターフェイス。 これは **[、IMAPIOfflineNotify のクライアントの実装です](imapiofflinenotifyiunknown.md)**。 
    
_ulAdviseTypes_: アドバイスの種類 。アドバイスの条件によって識別されます。 サポートされている唯一の型は、MAPIOFFLINE_ADVISE_TYPE_STATECHANGE。
    
_ulStateMask_: サポートされている唯一の状態は、MAPIOFFLINE_STATE_ALL。
    
## <a name="see-also"></a>関連項目

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [オフライン状態 API について](about-the-offline-state-api.md) 
- [MAPI �萔](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

