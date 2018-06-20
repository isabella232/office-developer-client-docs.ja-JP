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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6f17e501a90a50a4984cae470d3924205c78a604
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800637"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline: IUnknown

  
  
**適用されます**: Outlook 
  
オフライン オブジェクトの情報を提供します。
  
|||
|:-----|:-----|
|提供元:  <br/> |[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)に対してクエリを実行 <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |オフライン オブジェクトをオンラインまたはオフラインの現在の状態を設定します。  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |コールバックは、オフラインのオブジェクトによってサポートされている条件を取得します。  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |オフライン オブジェクトの現在のオンラインまたはオフラインの状態を取得します。  <br/> |
| *プレース ホルダー メンバー*  <br/> |このメンバーは、プレース ホルダーではサポートされていません。  <br/> |
   
## <a name="remarks"></a>備考

クライアントでは、 **[HrOpenOfflineObj](hropenofflineobj.md)** を使用して、開き、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。 ( [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)を使用) して、クライアントがこのインターフェイスを問い合わせることができます**IMAPIOfflineMgr**は、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)から継承しているため**IMAPIOffline**のオフラインのオブジェクトのインターフェイス ポインターへのポインターを取得します。 クライアントを取得または、オブジェクトの現在の状態を設定または ( **IMAPIOffline::GetCapabilities**の呼び出し) によって、オブジェクトのコールバック機能をお探しし、 **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** を使用してコールバックを設定する」を選択します。 
  
このインターフェイスのメンバーは、Microsoft Outlook 2013 の内部使用に予約されているプレース ホルダーし、変更されることが。 このインターフェイスの他のメンバーは、記載されている場合のみ使用してください。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)


[オフラインの状態の API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPI インターフェイス](mapi-interfaces.md)

