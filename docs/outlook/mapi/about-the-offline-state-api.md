---
title: オフライン状態 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410484"
---
# <a name="about-the-offline-state-api"></a>オフライン状態 API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン状態 API は、Microsoft Outlook 2013 および Microsoft Outlook 2010 でのユーザーの接続状態の変更を示すコールバックをサポートしています 。たとえば、Outlook 2013 または Outlook 2010 のオンライン状態からオフライン状態に変わるなどです。 API は、2013 年または Outlook 2010 年Outlookにグローバル オフライン オブジェクトを使用して、特定のユーザー アカウント プロファイルに対するこのような変更を追跡します。 通知は、サポートされているコールバックの唯一の形式です。 この API のクライアントとして、このような接続状態の変更を通知するメール プロバイダーは次の操作を行います。
  
1. **[IMAPIOfflineNotify を実装します](imapiofflinenotifyiunknown.md)**。 
    
2. **[HrOpenOfflineObj](hropenofflineobj.md)** を使用して、特定のプロファイルの既存のオフライン オブジェクトを開きます。 
    
3. オブジェクトが **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用してオンライン通知またはオフライン通知を提供できるかどうかを判断します。 
    
4. **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用して、オンラインまたはオフラインの通知のオブジェクトを登録します。 メール プロバイダーは **、IMAPIOfflineNotify** を使用して 2013 Outlook 2010 Outlook通知を受信できます。 
    
5. シャットダウン時に **[、IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** を使用してオンライン通知とオフライン通知の登録を削除します。 
    
> [!NOTE]
> 一般に、Outlook 2013 および Outlook 2010 は、オンライン/オフラインの変更と他の変更をクライアントに通知できますが、オフライン状態 API では、オンライン/オフラインの変更に関する通知のみをサポートしています。 クライアントは、他のすべての通知を無視する必要があります。 詳細については **[、「IMAPIOfflineNotify::Notify and MAPIOFFLINE_NOTIFY」](imapiofflinenotify-notify.md)** **[を参照してください](mapioffline_notify.md)**。 
  
 オフライン状態 API を使用するクライアントの例については、「サンプル オフライン状態アドインについて」 [を参照してください](about-the-sample-offline-state-add-in.md)。 サンプル オフライン状態アドインは、オフライン状態 API を使用して接続状態を監視および変更する COM アドインです。
  
この API は、次の機能を提供します。
  
定義:
  
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
    

