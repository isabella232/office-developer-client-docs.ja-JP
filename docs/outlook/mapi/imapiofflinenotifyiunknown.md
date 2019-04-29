---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439878"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft outlook 2010 および microsoft outlook 2013 をサポートしており、クライアントに対して通知コールバックを送信します。
  
|||
|:-----|:-----|
|提供元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |接続状態の変更についてクライアントに通知を送信します。  <br/> |
   
## <a name="remarks"></a>注釈

**[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** を使用してコールバックを設定する場合、クライアントはこのインターフェイスを実装し、 **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとしてのポインターを渡す必要があります。 その後、outlook 2010 または outlook 2013 は、このインターフェイスを使用して、クライアントに通知コールバックを送信できるようになります。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

