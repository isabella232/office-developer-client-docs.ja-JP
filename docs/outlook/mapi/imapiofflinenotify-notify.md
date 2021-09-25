---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 42c31247ad9c6445ddbe465539a2f35c6c601ea1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575898"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
接続状態の変更に関する通知をクライアントに送信します。
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>パラメーター

 _pNotifyInfo_
  
> [in]クライアントに送信Outlook通知。 通知は、変更された接続状態の一部、古い接続状態、および新しい接続状態を示します。
    
## <a name="remarks"></a>注釈

Outlookこのメソッドを使用して、クライアントに通知コールバックを送信します。 Microsoft Outlook 2010 または Microsoft Outlook 2013 でこのインターフェイスを使用するには **[、IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用してコールバックを設定するときに、クライアントでこのインターフェイスを実装し **[、MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとしてポインターを渡す必要があります。 
  
クライアントは、Outlook 2010 または Outlook 2013 が **IMAPIOfflineNotify::Notify** で使用するクライアント トークンを MAPIOFFLINE_ADVISEINFO に渡して、通知コールバックに登録されているクライアントを識別します。  
  
一般に、Outlook 2010 および Outlook 2013 は、オンライン/オフラインの変更や他の接続状態の変更をクライアントに通知できますが、オフライン状態 API では、オンライン/オフラインの変更に関する通知のみをサポートしています。 クライアントは、他のすべての通知を無視する必要があります。
  
## <a name="see-also"></a>関連項目



[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

