---
title: NoScribble 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 41f5acddf273de39a7d5952ccb00e868170c692d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801669"
---
# <a name="noscribble-state"></a>NoScribble 状態

  
  
**適用されます**: Outlook 
  
NoScribble 状態では、メッセージに対する変更が保存されていることを示します。 クライアント アプリケーションによってフォーム オブジェクトの[IPersistMessage::Save](ipersistmessage-save.md)メソッドが呼び出されたときに、フォーム オブジェクトのユーザー インターフェイスに格納されている値の実際の保存が発生します。 次の表では、NoScribble の状態から有効な遷移について説明します。 
  
|* IPersistMessage * 方法 * *|**アクション**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage = =_ NULL)  <br/> |_FSameAsLoad_フラグが TRUE の場合、NoScribble の状態と、メッセージを入力するフォームの原因となった[IPersistMessage::Save](ipersistmessage-save.md)の呼び出しが変更されて、内部的にマークの変更を保存して[IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)を呼び出すメソッドです。  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage! =_ NULL)  <br/> |**SaveCompleted**の通常の操作の後に (OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドのような) [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出します。 **SaveCompleted**が成功した場合は、通常の状態を入力します。 それ以外の場合、 [HandsOffAfterSave](handsoffaftersave-state.md)の状態を入力します。  <br/> |標準または HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |再帰的には、埋め込みメッセージでは、 **HandsOffMessage**メソッドまたは埋め込まれた OLE オブジェクトの OLE の**IPersistStorage::HandsOffStorage**メソッドを呼び出します。 メッセージ オブジェクトを解放し、埋め込みオブジェクトまたはメッセージ。  <br/> |HandsOffAfterSave  <br/> |
|**保存**、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、または[IPersistMessage::Load](ipersistmessage-load.md) <br/> |最後のエラーを設定、E_UNEXPECTED を返します。  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |NoScribble  <br/> |
|他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド  <br/> |最後のエラーを設定、E_UNEXPECTED を返します。  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)
