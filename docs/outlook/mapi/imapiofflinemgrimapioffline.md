---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 644fad96c8aec3701233351469a84ef93341b397
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800645"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr: IMAPIOffline

  
  
**適用されます**: Outlook 
  
ユーザー アカウントの接続状態の変更の通知コールバックの登録をサポートします。
  
|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[アドバイス](imapiofflinemgr-advise.md) <br/> |接続の変更についての通知コールバックを登録します。  <br/> |
|[アドバイズ中止します。](imapiofflinemgr-unadvise.md) <br/> |特定の通知コールバックの登録を削除します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
| *プレース ホルダー メンバー*  <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
   
## <a name="remarks"></a>備考

**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してユーザー ・ アカウント ・ プロファイルのオフラインのオブジェクトを開くには、クライアントは、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。 
  
( **[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)** を使用) して、クライアントがこのインターフェイスを問い合わせることができますこのインターフェイスは、 **[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)** から継承しているため**[IMAPIOffline](imapiofflineiunknown.md)** をサポートしているオブジェクトを取得します。 クライアント (呼び出し元**[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** )、オフライン オブジェクトのコールバック機能をお探しし、( **IMAPIOfflineMgr::Advise**を使用) でのコールバックを設定する」を選択します。 
  
このインターフェイスのメンバーのほとんどは、Outlook の内部使用に予約されているプレース ホルダーであるし、変更されることが。 このインターフェイスの呼び出し元は、プレース ホルダー以外のメンバーを使用して、記載されている場合にのみ必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIOffline: IUnknown](imapiofflineiunknown.md)


[オフラインの状態の API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[MAPI インターフェイス](mapi-interfaces.md)
