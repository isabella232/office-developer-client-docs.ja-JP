---
title: オフライン状態 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321792"
---
# <a name="about-the-offline-state-api"></a>オフライン状態 API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン状態 API は、microsoft outlook 2013 および microsoft outlook 2010 でユーザーの接続状態が変更されたことを示すコールバックをサポートします (たとえば、outlook 2013 または outlook 2010 でオフラインになっている場合)。 この API は、outlook 2013 または outlook 2010 のグローバルオフラインオブジェクトを使用して、特定のユーザーアカウントプロファイルに対する変更を追跡します。 通知は、サポートされているコールバックの唯一の形式です。 この API のクライアントとして、このような接続状態の変更を通知するメールプロバイダーは、次の操作を行います。
  
1. **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を実装します。 
    
2. **[hro・ offlineofflineobj](hropenofflineobj.md)** を使用して、特定のプロファイルの既存のオフラインオブジェクトを開きます。 
    
3. オブジェクトに、 **[imapioffline:: getcapabilities](imapioffline-getcapabilities.md)** を使用してオンラインまたはオフライン通知を提供する機能があるかどうかを判断します。 
    
4. **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** を使用して、オブジェクトをオンライン通知またはオフライン通知用に登録します。 メールプロバイダーは、outlook 2013 または outlook 2010 で**IMAPIOfflineNotify**を使用して送信された通知を受信できるようになります。 
    
5. シャットダウン時に、 **[IMAPIOfflineMgr:: アドバイズ](imapiofflinemgr-unadvise.md)** 中止を使用してオンラインおよびオフライン通知の登録を削除します。 
    
> [!NOTE]
> 一般に、outlook 2013 および outlook 2010 は、オンライン/オフライン変更のクライアントに加えて、他の変更を通知することができますが、オフライン状態 API はオンライン/オフラインの変更に関する通知のみをサポートしています。 クライアントは、他のすべての通知を無視する必要があります。 詳細については、「 **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**」を参照してください。 
  
 オフライン状態 API を使用するクライアントの例については、「[サンプルのオフライン状態アドインについ](about-the-sample-offline-state-add-in.md)て」を参照してください。 サンプルのオフライン状態アドインは、オフライン状態 API を使用して接続状態を監視および変更する COM アドインです。
  
この API は、次の機能を提供します。
  
定義
  
- [MAPI �萔](mapi-constants.md)
    
データ型:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
関数
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
インターフェイス
  
- **[imapioffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

