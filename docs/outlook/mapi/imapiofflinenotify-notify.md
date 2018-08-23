---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800644"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**適用対象**: Outlook 
  
接続状態の変更についてクライアントに通知を送信します。
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>パラメーター

 _pNotifyInfo_
  
> [in]Outlook をクライアントに送信する通知します。 通知では、接続状態が変更されたこと、以前の接続状態、および新しい接続の状態の一部を示します。
    
## <a name="remarks"></a>注釈

Outlook では、このメソッドを使用して、通知のコールバックをクライアントに送信します。 Microsoft Outlook 2010 または Microsoft Outlook 2013 にこのインターフェイスを使用できるようにするには、クライアントする必要がありますこのインターフェイスを実装し、 **[IMAPIOfflineMgr::Advise を使用してコールバックをセットアップするときの**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとして、それへのポインターを渡す](imapiofflinemgr-advise.md)**. 
  
クライアントもトークンを渡します**MAPIOFFLINE_ADVISEINFO**に、クライアントを Outlook 2010 または Outlook 2013 では、 **IMAPIOfflineNotify::Notify**の通知コールバックの登録されているクライアントを識別します。 
  
一般に、Outlook 2010、Outlook 2013 は、オンラインとオフラインの変更のクライアントおよびその他の接続状態の変更を通知できますが、オフライン状態の API は、オンラインとオフラインの変更の通知のみをサポートしています。 クライアントは、他のすべての通知を無視する必要があります。
  
## <a name="see-also"></a>関連項目



[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

