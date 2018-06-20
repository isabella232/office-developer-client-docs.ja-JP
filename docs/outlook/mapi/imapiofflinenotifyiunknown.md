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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 37f21c438a0a337eecf5c15a27a0b891d19bcfb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800632"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify: IUnknown

  
  
**適用されます**: Outlook 
  
通知コールバックをクライアントに送信するのには、Microsoft Outlook 2010 と Microsoft Outlook 2013 をサポートしています。
  
|||
|:-----|:-----|
|提供元:  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |接続状態の変更についてクライアントに通知を送信します。  <br/> |
   
## <a name="remarks"></a>備考

クライアントは、このインターフェイスを実装し、 **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用してコールバックをセットアップするときの**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとして、それへのポインターを渡す必要があります。 その後、Outlook 2010 または Outlook 2013 できるようになります通知コールバックをクライアントに送信するのにはこのインターフェイスを使用します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[オフラインの状態の API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

