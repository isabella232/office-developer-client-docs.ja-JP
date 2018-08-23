---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587132"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームの閲覧者は、フォーム ビューのコンテキストと、フォームの動詞を実行して、フォームをシャット ダウンするのにはフォームの通知を有効にします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |フォーム オブジェクト  <br/> |
|によって実装されます。  <br/> |フォーム サーバー  <br/> |
|によって呼び出されます。  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIForm  <br/> |
|ポインターの型。  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |フォームのビュー コンテキストを確立します。  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |フォームの現在のビュー コンテキストを返します。  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |フォームを閉じます。  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |フォームは、タスクをどのような実行要求は、特定の動作に関連付けます。  <br/> |
|[アドバイス](imapiform-advise.md) <br/> |フォーム ビューアーの形式に影響するイベント通知を登録します。  <br/> |
|[アドバイズ中止します。](imapiform-unadvise.md) <br/> |**アドバイズ**を呼び出すことによって確立されていたフォーム ビューアーを使用して通知の登録をキャンセルします。  <br/> |
|[発生しました](imapiform-getlasterror.md) <br/> |前の form オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

