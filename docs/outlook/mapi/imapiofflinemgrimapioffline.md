---
title: IMAPIOfflineMgr imapioffline
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 235c2afb20e6f36df72eac4070c1df5fd10fcce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270092"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーアカウントの接続状態の変更に関する通知コールバックの登録をサポートします。
  
|||
|:-----|:-----|
|エクスポート対象:  <br/> |msmapi32  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[助言](imapiofflinemgr-advise.md) <br/> |接続の変更に関する通知コールバックを登録します。  <br/> |
|[アドバイズ](imapiofflinemgr-unadvise.md) <br/> |通知コールバックの指定された登録を削除します。  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
| *Placeholder メンバー*  <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
   
## <a name="remarks"></a>解説

**[hroな offlineobj](hropenofflineobj.md)** を使用してユーザーアカウントプロファイルのオフラインオブジェクトを開くと、クライアントは**IMAPIOfflineMgr**をサポートするオフラインオブジェクトを取得します。 
  
このインターフェイスは**[iunknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** から継承されるため、クライアントはこのインターフェイスを ( **[iunknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** を使用して) 照会して、 **[imapioffline](imapiofflineiunknown.md)** をサポートするオブジェクトを取得できます。 クライアントは、oab ( **[imapioffline:: getcapabilities](imapioffline-getcapabilities.md)** ) を呼び出すことによって、オフラインオブジェクトのコールバック機能について調べることができます。また、( **IMAPIOfflineMgr:: Advise**を使用して) コールバックの設定を選択することもできます。 
  
このインターフェイスのメンバーのほとんどは、Outlook の内部使用のために予約されたプレースホルダーであり、変更される可能性があります。 このインターフェイスの発信者は、ドキュメント化されている場合にのみ、プレースホルダー以外のメンバーを使用する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[MAPI のインターフェイス](mapi-interfaces.md)

