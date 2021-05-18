---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321267"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン オブジェクトの情報を提供します。
  
|||
|:-----|:-----|
|提供元:  <br/> |[IMAPIOfflineMgr のクエリ](imapiofflinemgrimapioffline.md) <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |オフライン オブジェクトの現在の状態をオンラインまたはオフラインに設定します。  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |オフライン オブジェクトでコールバックがサポートされる条件を取得します。  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |オフライン オブジェクトの現在のオンライン状態またはオフライン状態を取得します。  <br/> |
| *プレースホルダー メンバー*  <br/> |このメンバーはプレースホルダーであり、サポートされていません。  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは **[、HrOpenOfflineObj](hropenofflineobj.md)** を使用して **、IMAPIOfflineMgr** をサポートするオフライン オブジェクトを開いて取得します。 **IMAPIOfflineMgr** は [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から継承しますので、クライアントは [(IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を使用して) このインターフェイスをクエリして、オフライン オブジェクトの **IMAPIOffline** のインターフェイス ポインターへのポインターを取得できます。 その後、クライアントはオブジェクトの現在の状態を取得または設定するか、オブジェクトのコールバック機能 **(IMAPIOffline::GetCapabilities** を呼び出して) を確認し **[、IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** を使用してコールバックを設定できます。 
  
このインターフェイスのメンバーは、内部で使用するために予約されたプレースホルダーであり、Microsoft Outlook 2013変更される場合があります。 このインターフェイスの他のメンバーは、ドキュメントとしてのみ使用する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPI のインターフェイス](mapi-interfaces.md)

