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
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410694"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
接続状態の変更についてクライアントに通知を送信します。
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>パラメーター

 _pnotifyinfo_
  
> 順番Outlook からクライアントに送信される通知。 通知は、変更された接続状態の一部、古い接続状態、および新しい接続状態を示します。
    
## <a name="remarks"></a>注釈

Outlook では、このメソッドを使用して通知コールバックをクライアントに送信します。 このインターフェイスを microsoft outlook 2010 または microsoft outlook 2013 が使用できるようにするには、クライアントはこのインターフェイスを実装し、 **[](mapioffline_adviseinfo.md)** **[IMAPIOfflineMgr:: Advise を使用してコールバックを設定するときに、MAPIOFFLINE_ADVISEINFO のメンバーとしてのポインターを渡す必要があります。](imapiofflinemgr-advise.md)**. 
  
また、クライアントは、outlook 2010 または outlook 2013 が**IMAPIOfflineNotify:: Notify**で使用するクライアントトークンを**MAPIOFFLINE_ADVISEINFO**に渡して、通知コールバック用に登録されているクライアントを識別します。 
  
一般に、outlook 2010 および outlook 2013 は、オンライン/オフラインの変更やその他の接続状態の変更をクライアントに通知します。ただし、オフライン状態 API はオンライン/オフラインの変更に関する通知のみをサポートしています。 クライアントは、他のすべての通知を無視する必要があります。
  
## <a name="see-also"></a>関連項目



[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

