---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801516"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**適用対象**: Outlook 
  
これは、接続状態の変更を通知します。 接続状態が変更されたこと、以前の接続状態、および新しい接続の状態の一部を示します。
  
## <a name="quick-info"></a>クイック ヒント

**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を参照してください。 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a>Members

 _ulSize_
  
> **MAPIOFFLINE_NOTIFY**構造体のサイズです。 
    
 _NotifyType_
  
> 通知の種類です。 接続状態の変更時にのみ通知がサポートされることに注意してください。のみサポートされている値は次のとおりです。
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> クライアントが**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** の**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** 構造体で定義されているトークンです。 
    
 _ulMask_
  
> 接続の状態が変更されたことの一部です。 唯一のサポートされている値は、MAPIOFFLINE_STATE_OFFLINE_MASK です。
    
 _ulStateOld_
  
> 古い接続状態です。 のみサポートされている値は次のとおりです。
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> 新しい接続状態です。 のみサポートされている値は次のとおりです。
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>注釈

オフラインの状態の API では、オンラインとオフラインの変更の通知のみをサポートしています。 クライアントは、Outlook が実際の変更を確認する前に次の値を返すことを確認する必要があります。
  
1.  *NotifyType*には、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE、または MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE の値があります。 この例では、クライアントは、変更は、接続状態の変更*の*構造体の*情報*と想定できます。 
    
2.  *ulMask*には、MAPIOFFLINE_STATE_OFFLINE_MASK の値があります。 この例では、クライアントは、オンラインとオフラインの接続状態の変更、および*ulStateOld*と*ulStateNew*の確認を行うことを想定できます。 
    
Outlook がサポートされていないその他の変更のクライアントに通知することができます。 このような場合、 *NotifyType*できません、上記 3 つの値のいずれかのや*ulMask*には、MAPIOFFLINE_STATE_OFFLINE_MASK ができないクライアントは、*情報*では、データの残りの部分を無視する必要があります。 
  
## <a name="see-also"></a>関連項目

- [オフライン状態 API について](about-the-offline-state-api.md)  
- [MAPI �萔](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

