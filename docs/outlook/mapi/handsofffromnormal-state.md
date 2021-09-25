---
title: HandsOffFromNormal State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45374bfbead9f8f94967149c1f418cf77aa9ebd3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561727"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal State

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
HandsOffFromNormal 状態は [、HandsOffAfterSave 状態と非常に似](handsoffaftersave-state.md) ています。 これは、フォームの内容を永続的な記憶域に保存するプロセスの一部です。 この状態の場合、フォーム オブジェクトは、メッセージのプロパティの値のメモリ内コピーに変更を加えるのを控える必要があります。これらの変更を保存する別の機会が存在しない可能性があります。 次の表では、HandsOffFromNormal 状態からの許可された移行について説明します。 
  
|IPersistMessage** メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |メッセージ オブジェクトのメッセージを  _pMessage_ に置き換え [、IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)の前の呼び出しによって取り消されたメッセージの代わりに使用します。 新しいメッセージのデータは、取り消されたメッセージと同じになる必要があります。 メッセージをクリーンとしてマークしたり [、IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) をこの呼び出し後に呼び出したりする必要もありません。 **SaveCompleted 呼び出しが** 成功した場合は、Normal 状態 [を入力](normal-state.md)します。 それ以外の場合は、HandsOffFromNormal 状態にとどまります。  <br/> |Normal または HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |最後のエラーを [エラー] にE_UNEXPECTED。  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**、 [IPersistMessage::Save](ipersistmessage-save.md)、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、 [または IPersistMessage::Load](ipersistmessage-load.md) <br/> |最後のエラーを [エラー] にE_UNEXPECTED。  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |HandsOffFromNormal  <br/> |
|その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド  <br/> |最後のエラーを [エラー] にE_UNEXPECTED。  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

