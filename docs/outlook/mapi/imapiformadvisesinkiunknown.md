---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286605"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーがフォームビューアーから通知を受信できるようにします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |Form アドバイズシンクオブジェクト  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォームビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |フォームビューアーの状態で変更が発生したことを示します。  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |フォームが次に表示されるメッセージのメッセージクラスを処理できるかどうかを示します。  <br/> |
   
## <a name="remarks"></a>解説

フォームサーバーは form アドバイズシンクオブジェクトを使用して、form オブジェクトに含めるのではなく、 **IMAPIFormAdviseSink**を実装します。 そのため、フォーム閲覧者は、このインターフェイスへのポインターを取得するために、フォームの[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドへの呼び出しが失敗したことを想定してください。 
  
フォームサーバーは、通知を登録するために、ビューアーの[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。 **IMAPIFormAdviseSink**実装へのポインターは、パラメーターとして含まれています。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

