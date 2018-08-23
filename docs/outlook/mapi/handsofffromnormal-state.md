---
title: HandsOffFromNormal 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 92c604c621e2837b76e9e49fd182524ad17fbcac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588343"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal 状態

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
HandsOffFromNormal 状態では、 [HandsOffAfterSave](handsoffaftersave-state.md)の状態に非常に似ています。 恒久的ストレージにフォームの内容を保存するプロセスの一部です。 この状態のときにフォーム オブジェクト避ける必要がある、メモリ内のコピー、メッセージのプロパティの値を変更するため、別の機会をこれらの変更を保存することができません。 次の表では、HandsOffFromNormal の状態から有効な遷移について説明します。 
  
|* IPersistMessage * 方法 * *|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage! =_ NULL)  <br/> |メッセージ オブジェクトのメッセージを交換して、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)の以前の呼び出しによって無効にするメッセージの交換が_pMessage_と。 失効したメッセージと同じにする、新しいメッセージ内のデータが保証されます。 メッセージがクリーンとしてマークされていない必要がありますもする必要があります[IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)はこの呼び出しの後呼び出されます。 **SaveCompleted**の呼び出しが成功した場合は、[通常](normal-state.md)の状態を入力します。 それ以外の場合、HandsOffFromNormal の状態のままです。  <br/> |標準または HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage = =_ NULL)  <br/> |E_UNEXPECTED を最後にエラーを設定します。  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**、 [IPersistMessage::Save](ipersistmessage-save.md)、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、または[IPersistMessage::Load](ipersistmessage-load.md) <br/> |E_UNEXPECTED を最後にエラーを設定します。  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |HandsOffFromNormal  <br/> |
|他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド  <br/> |E_UNEXPECTED を最後にエラーを設定します。  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

