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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286605"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム サーバーがフォーム ビューアーから通知を受け取ることができます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォームアアドバイスシンク オブジェクト  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォーム ビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |フォーム ビューアーの状態で変更が発生したかどうかを示します。  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |表示する次のメッセージのメッセージ クラスをフォームで処理できるかどうかを示します。  <br/> |
   
## <a name="remarks"></a>注釈

フォーム サーバーでは、フォーム オブジェクトに **IMAPIFormAdviseSink** を含める代わりに、フォーム アアドバイス シンク オブジェクトを使用して IMAPIFormAdviseSink を実装します。 したがって、フォーム ビューアーは、このインターフェイスへのポインターを取得するために、フォームの [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) メソッドへの呼び出しが失敗したと予想する必要があります。 
  
フォーム サーバーは、ビューアーの [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) メソッドを呼び出して、通知に登録します。 **IMAPIFormAdviseSink** 実装へのポインターがパラメーターとして含まれます。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

