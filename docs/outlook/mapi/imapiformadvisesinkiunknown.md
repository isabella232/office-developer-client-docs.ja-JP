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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800517"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink: IUnknown

  
  
**適用されます**: Outlook 
  
フォームの閲覧者から通知を受信するフォームのサーバーを使用できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |シンク オブジェクトをフォームに伝えます。  <br/> |
|によって実装されます。  <br/> |フォーム サーバー  <br/> |
|によって呼び出されます。  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |フォーム ビューアーのステータスに変更が発生したことを示します。  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。  <br/> |
   
## <a name="remarks"></a>備考

フォーム、フォームのサーバーの使用は、そのフォーム オブジェクトに含めての代わりに**IMAPIFormAdviseSink**を実装するシンク オブジェクトを案内します。 したがって、フォームの閲覧者はこのインターフェイスへのポインターを取得するフォームの[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)メソッドに失敗した呼び出しを想定します。 
  
フォーム サーバーでは、通知を登録するのには、ビューアーの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。 **IMAPIFormAdviseSink**実装へのポインターでは、パラメーターとして含まれています。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

