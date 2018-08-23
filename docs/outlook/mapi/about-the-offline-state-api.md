---
title: オフライン状態 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: aa30a173251193d74d6560c8dce2663463a18e36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565985"
---
# <a name="about-the-offline-state-api"></a>オフライン状態 API について

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オフラインの状態の API は、Microsoft Outlook 2013 および Microsoft Outlook 2010 でのユーザーの接続状態の変化を示すコールバックをサポートしています: からのオフライン中に Outlook 2013 または Outlook 2010 でオンラインにします。 API は、特定のユーザー ・ アカウント ・ プロファイルには、このような変更を追跡するために Outlook 2013 または Outlook 2010 でのオフラインのグローバル オブジェクトを使用します。 通知は、コールバックの形式でのみサポートされています。 この API のクライアントとしてこのような接続状態の変更の通知を受ける必要があるメールのプロバイダー、次の操作を行います。
  
1. **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を実装します。 
    
2. **[HrOpenOfflineObj](hropenofflineobj.md)** を使用して特定のプロファイルに既存のオフライン オブジェクトを開きます。 
    
3. オブジェクトに**[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用して、オンラインまたはオフラインの通知を提供する機能があるかどうかを決定します。 
    
4. **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用して通知をオンラインまたはオフラインのオブジェクトを登録します。 メール プロバイダーでは、2013 の Outlook または Outlook 2010 送信する**IMAPIOfflineNotify**を使用して通知を受信できるようになりました。 
    
5. シャット ダウン時に**[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** を使用して、オンラインとオフラインの通知の登録を削除します。 
    
> [!NOTE]
> 一般に、Outlook 2013 と Outlook 2010 のオンライン/オフラインでの変更とその他の変更は、クライアントに通知できますが、オフライン状態の API は、オンラインとオフラインの変更の通知のみをサポートしています。 クライアントは、他のすべての通知を無視してください。 詳細については、 **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** および**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** を参照してください。 
  
 オフライン状態 API を使用するクライアントの例は、[のサンプル オフライン状態がアドインを](about-the-sample-offline-state-add-in.md)参照してください。 オフライン状態のサンプル アドインは、COM アドインの API を使用して、オフラインの状態を監視し、接続状態を変更します。
  
この API には、次のものが用意されています。
  
定義
  
- [MAPI �萔](mapi-constants.md)
    
データ型:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
関数
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
インターフェイス
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

