---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b61a4017ee8763e07647b1f4c3eca6fef7d4fe2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630692"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザー アカウントの接続状態の変更に関する通知コールバックの登録をサポートします。
  
|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[アドバイス](imapiofflinemgr-advise.md) <br/> |接続の変更に関する通知コールバックを登録します。  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |通知コールバックの特定の登録を削除します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
| *プレースホルダー メンバー*  <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
   
## <a name="remarks"></a>注釈

**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してユーザー アカウント プロファイルのオフライン オブジェクトを開いた後、クライアントは **IMAPIOfflineMgr** をサポートするオフライン オブジェクトを取得します。 
  
このインターフェイスは **[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** から継承されますので、クライアントは **[(IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** を使用して) このインターフェイスを照会して **[、IMAPIOffline](imapiofflineiunknown.md)** をサポートするオブジェクトを取得できます。 クライアントは、オフライン オブジェクトのコールバック機能 **[(IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を呼び出すことによって) を確認し **、(IMAPIOfflineMgr::Advise** を使用して) コールバックを設定します。 
  
このインターフェイスのメンバーの大部分は、内部で使用するために予約されたプレースホルダーであり、Outlook変更される場合があります。 このインターフェイスの呼び出し元は、文書化されているプレースホルダー以外のメンバーのみを使用する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[MAPI のインターフェイス](mapi-interfaces.md)

