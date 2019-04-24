---
title: imapioffline IUnknown
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321267"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフラインオブジェクトに関する情報を提供します。
  
|||
|:-----|:-----|
|提供元:  <br/> |[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)のクエリ <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|**[setlevel](imapioffline-setcurrentstate.md)** <br/> |オフラインオブジェクトの現在の状態をオンラインまたはオフラインに設定します。  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |オフラインオブジェクトでサポートされているコールバックの条件を取得します。  <br/> |
|**[getselected](imapioffline-getcurrentstate.md)** <br/> |オフラインオブジェクトの現在のオンライン状態またはオフライン状態を取得します。  <br/> |
| *Placeholder メンバー*  <br/> |このメンバーはプレースホルダーで、サポートされていません。  <br/> |
   
## <a name="remarks"></a>解説

クライアントは**[hropenofflineobj](hropenofflineobj.md)** を使用して、 **IMAPIOfflineMgr**をサポートするオフラインオブジェクトを開いて取得します。 **IMAPIOfflineMgr**は[iunknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)から継承するため、クライアントはこのインターフェイスを ( [iunknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を使用して) 照会し、オフラインオブジェクトの**imapioffline**のインターフェイスポインターへのポインターを取得することができます。 クライアントは、オブジェクトの現在の状態を取得または設定したり、オブジェクトのコールバック機能 ( **imapioffline:: getcapabilities**を呼び出すことによって) を調べたり、 **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** を使用してコールバックを設定したりすることができます。 
  
このインターフェイスのメンバーは、Microsoft Outlook 2013 の内部使用のために予約されているプレースホルダーであり、変更される可能性があります。 このインターフェイスの他のメンバーは、ドキュメント化されている場合にのみ使用する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPI のインターフェイス](mapi-interfaces.md)

