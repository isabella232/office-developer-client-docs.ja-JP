---
title: 通常の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dcc92d220f07b1c111284acacac4a65a2e3f8b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801659"
---
# <a name="normal-state"></a>通常の状態

  
  
**適用されます**: Outlook 
  
通常の状態では、form オブジェクトが変更を保存するか、フォームを閉じるなどの操作を開始するクライアント アプリケーションを待機して、その時間のほとんどを費やしています。 次の表では、通常の状態から有効な遷移について説明します。
  
|**IPersistMessage メソッド**|**アクション**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage = =_ NULL _fSameAsLoad = =_ TRUE)  <br/> または  <br/> **IPersistMessage::Save**(_pMessage! =_ NULL _fSameAsLoad = =_ は FALSE)  <br/> |保存に変更されたすべての埋め込み OLE オブジェクトを再帰的にします。 メッセージ オブジェクトには、メッセージ データを保存します。 [NoScribble](noscribble-state.md)状態で後で使用できる_fSameAsLoad_フラグを格納します。  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage! =_ NULL _fSameAsLoad = =_ TRUE)  <br/> |これは、この**保存**の呼び出しはメモリ不足の状況で使用され、メモリ不足によって失敗する必要がありますが、前の例と同じです。  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |再帰的には、埋め込みメッセージでは、 **HandsOffMessage**メソッドまたは埋め込まれた OLE オブジェクトの OLE の[IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドを呼び出します。 メッセージ オブジェクトを解放し、埋め込みオブジェクトまたはメッセージ。  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)または[IPersistMessage::Load](ipersistmessage-load.md) <br/> |最後のエラーを設定、E_UNEXPECTED を返します。  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |Normal  <br/> |
|他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたはその他のインターフェイスのメソッド  <br/> |マニュアルで説明するように実装、 [IPersistMessage: IUnknown](ipersistmessageiunknown.md)インタ フェースです。  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

