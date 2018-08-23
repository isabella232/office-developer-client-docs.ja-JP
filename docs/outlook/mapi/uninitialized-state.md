---
title: Uninitialized 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c00d5bb2e5da02b007579c7a8206baa98f64143f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804164"
---
# <a name="uninitialized-state"></a>Uninitialized 状態

  
  
**適用対象**: Outlook 
  
初期化されていない状態は、オブジェクトが最初に作成されたときにする必要があります初期状態のフォームです。 フォーム オブジェクトは、クライアント アプリケーションは、フォーム オブジェクトの[IPersistMessage::InitNew](ipersistmessage-initnew.md)または[IPersistMessage::Load](ipersistmessage-load.md)メソッドを呼び出すと、メッセージ データで初期化になります。 次の表では、Unitialized の状態から有効な遷移について説明します。 
  
|**IPersistMessage メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |フォーム オブジェクトに既定のデータをロードします。  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |移行先のメッセージには、フォーム オブジェクトにデータを読み込みます。  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |成功した場合、または最後のエラーに設定を返し、E_UNEXPECTED を返します。  <br/> |初期化されていません  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |初期化されていません  <br/> |
|他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド  <br/> |最後のエラーを設定、E_UNEXPECTED を返します。  <br/> |初期化されていません  <br/> |
   
## <a name="see-also"></a>関連項目



[Normal 状態](normal-state.md)
  
[フォームの状態](form-states.md)

