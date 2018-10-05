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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392061"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの閲覧者から通知を受信するフォームのサーバーを使用できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |シンク オブジェクトをフォームに伝えます。  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |フォーム ビューアーのステータスに変更が発生したことを示します。  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。  <br/> |
   
## <a name="remarks"></a>備考

フォーム、フォームのサーバーの使用は、そのフォーム オブジェクトに含めての代わりに**IMAPIFormAdviseSink**を実装するシンク オブジェクトを案内します。 したがって、フォームの閲覧者はこのインターフェイスへのポインターを取得するフォームの[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドに失敗した呼び出しを想定します。 
  
フォーム サーバーでは、通知を登録するのには、ビューアーの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。 **IMAPIFormAdviseSink**実装へのポインターでは、パラメーターとして含まれています。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

