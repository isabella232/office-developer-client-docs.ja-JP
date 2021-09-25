---
title: HandsOffAfterSave 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9027ab37fe5183847ee8181530f9adb1a8cddde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551465"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave 状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
HandsOffAfterSave 状態は、フォームの内容を永続的な記憶域に保存するプロセスの一部です。 この状態の場合、フォーム オブジェクトは、メッセージのプロパティの値のメモリ内コピーに変更を加えるのを控える必要があります。これらの変更を保存する別の機会が存在しない可能性があります。 次の表では、HandsOffAfterSave 状態からの許可された移行について説明します。
  
|**IPersistMessage メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |埋め込みオブジェクトを開きます。 _pMessage_ に格納されているメッセージ内のデータは、前の [IPersistMessage::Save](ipersistmessage-save.md)呼び出しのメッセージと同じになる必要があります。 **SaveCompleted 呼び出しが** 成功した場合は、Normal 状態を入力します。 それ以外の場合は、最後のエラーを [E_OUTOFMEMORYに設定し、HandsOffAfterSave 状態に残ります。  <br/> |[Normal または](normal-state.md) HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |最後のエラーを[エラー] または [E_INVALIDARG] にE_UNEXPECTED。  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) **、Save、**[または IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |ターゲット メッセージのデータを含むフォーム オブジェクトを読み込む。 この呼び出しは、フォーム オブジェクトがフォルダー内の次または前のメッセージに移動するときに発生する可能性があります。  <br/> |標準  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |HandsOffAfterSave  <br/> |
|その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド  <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

