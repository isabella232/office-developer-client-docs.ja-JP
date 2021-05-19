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
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**適用対象**: Outlook 2013 | Outlook 2016 
  
これは、接続状態の変更に関する通知です。 これは、変更された接続状態の一部、古い接続状態、および新しい接続状態を示します。
  
## <a name="quick-info"></a>クイック ヒント

**[「IMAPIOfflineNotify」を参照してください](imapiofflinenotifyiunknown.md)**。 
  
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
  
> 構造体の **サイズMAPIOFFLINE_NOTIFY** します。 
    
 _NotifyType_
  
> 通知の種類。 接続状態の変更に関する通知だけがサポートされています。サポートされている値は次のとおりです。
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)****[の](mapioffline_adviseinfo.md)** MAPIOFFLINE_ADVISEINFOでクライアントによって定義されたトークンです。 
    
 _ulMask_
  
> 変更された接続状態の部分。 サポートされている唯一の値は、MAPIOFFLINE_STATE_OFFLINE_MASK。
    
 _ulStateOld_
  
> 古い接続状態。 サポートされている値は次のとおりです。
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> 新しい接続状態。 サポートされている値は次のとおりです。
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>注釈

オフライン状態 API は、オンライン/オフラインの変更に関する通知のみをサポートします。 クライアントは、実際の変更Outlook前に、次の値を返す必要があります。
  
1.  *NotifyType*  には、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE、またはMAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE。 この場合、クライアントは、変更が接続状態の変更であり  *、Info*  が  *StateChange 構造であると仮定できます*  。 
    
2.  *ulMask には*  、値がMAPIOFFLINE_STATE_OFFLINE_MASK。 この場合、クライアントは変更がオンライン/オフラインの接続状態の変更と見なして  *、ulStateOld*  と  *ulStateNew*  の検査を続行できます。 
    
サポートされていないその他Outlookクライアントに通知する可能性があります。 このような場合  *、NotifyType*  は前に述べた 3 つの値の 1 つで、または  *ulMask*  は MAPIOFFLINE_STATE_OFFLINE_MASK ではなく、クライアントは  *Info*  の残りのデータを無視する必要があります。 
  
## <a name="see-also"></a>関連項目

- [オフライン状態 API について](about-the-offline-state-api.md)  
- [MAPI �萔](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

