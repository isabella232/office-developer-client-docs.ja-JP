---
title: HandsOffAfterSave 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564536"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave 状態

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
HandsOffAfterSave の状態は、恒久的に保存するフォームの内容を保存するプロセスの一部です。 この状態のときにフォーム オブジェクト避ける必要がある、メモリ内のコピー、メッセージのプロパティの値を変更するため、別の機会をこれらの変更を保存することができません。 次の表では、HandsOffAfterSave の状態から有効な遷移について説明します。
  
|**IPersistMessage メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage! =_ NULL)  <br/> |埋め込みオブジェクトを開きます。 _PMessage_に格納されているメッセージ内のデータを保証して、以前の[IPersistMessage::Save](ipersistmessage-save.md)の呼び出し内のメッセージと同じであります。 **SaveCompleted**の呼び出しが成功した場合は、通常の状態を入力します。 それ以外の場合、E_OUTOFMEMORY を最後にエラーを設定し、HandsOffAfterSave 状態のままです。  <br/> |[標準](normal-state.md)または HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage = =_ NULL)  <br/> |E_INVALIDARG、E_UNEXPECTED を最後にエラーを設定します。  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)、**保存**、または[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |最後のエラーを設定、E_UNEXPECTED を返します。  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |移行先のメッセージには、フォーム オブジェクトにデータを読み込みます。 この呼び出しは、フォーム オブジェクトがフォルダー内の次または前のメッセージを移動したときに発生します。  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |HandsOffAfterSave  <br/> |
|他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド  <br/> |最後のエラーを設定、E_UNEXPECTED を返します。  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

