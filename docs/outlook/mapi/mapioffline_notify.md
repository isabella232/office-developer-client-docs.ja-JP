---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414768"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**適用対象**: Outlook 2013 | Outlook 2016 
  
これは、接続状態の変更に対する通知です。 この値は、変更された接続状態の部分、古い接続状態、および新しい接続状態を示します。
  
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

## <a name="members"></a>メンバー

 _ulsize_
  
> **MAPIOFFLINE_NOTIFY**構造体のサイズ。 
    
 _notifytype_
  
> 通知の種類。 接続状態の変更に関する通知のみがサポートされることに注意してください。サポートされている値は次のとおりです。
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulclienttoken_
  
> **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** の**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** 構造でクライアントによって定義されたトークン。 
    
 _ulmask_
  
> 変更された接続状態の部分。 サポートされている値は MAPIOFFLINE_STATE_OFFLINE_MASK のみです。
    
 _ulstateold_
  
> 古い接続状態。 サポートされている値は次のとおりです。
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> 新しい接続状態。 サポートされている値は次のとおりです。
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>注釈

オフライン状態 API は、オンライン/オフラインの変更についてのみ通知をサポートしています。 クライアントは、実際の変更を検査する前に、Outlook が次の値を返すことを確認する必要があります。
  
1.  *notifytype*には、値 MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE、または MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE があります。 この例では、クライアントは、変更が接続状態の変更であると想定し、 *Info*は*StateChange*構造になっています。 
    
2.  *ulmask*の値は MAPIOFFLINE_STATE_OFFLINE_MASK です。 この場合、クライアントは、変更がオンライン/オフラインの接続状態に変更されたと見なすことができ、 *ulstateold*および*ulStateNew*の調査に進むことができます。 
    
Outlook は、サポートされていない他の変更をクライアントに通知することができます。 このような場合、 *notifytype*は、前に示した3つの値のいずれかにはなりません。また*ulmask*は MAPIOFFLINE_STATE_OFFLINE_MASK されず、クライアントは*Info*の残りのデータを無視する必要があります。 
  
## <a name="see-also"></a>関連項目

- [オフライン状態 API について](about-the-offline-state-api.md)  
- [MAPI �萔](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

