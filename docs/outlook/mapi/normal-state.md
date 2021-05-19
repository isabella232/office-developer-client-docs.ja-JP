---
title: 標準状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335744"
---
# <a name="normal-state"></a>標準状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Normal 状態は、フォーム オブジェクトがほとんどの時間を費やし、クライアント アプリケーションが変更の保存やフォームの終了などのアクションを開始するのを待つ状態です。 次の表に、Normal 状態からの移行を許可する方法を示します。
  
|**IPersistMessage メソッド**|**Action**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> または  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |変更された埋め込み OLE オブジェクトを再帰的に保存します。 メッセージ データをメッセージ オブジェクトに保存します。 後で  _使用する fSameAsLoad_ フラグを [NoScribble 状態に格納](noscribble-state.md) します。  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |これは、前のケースと同じですが、このSave 呼び出しはメモリ不足の状況で使用され、メモリ不足のために失敗しはしません。  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |埋め込みメッセージ **の HandsOffMessage** メソッド、または埋め込み OLE オブジェクトの OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) メソッドを再帰的に呼び出します。 メッセージ オブジェクトと埋め込みメッセージまたはオブジェクトを解放します。  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) または [IPersistMessage::Load](ipersistmessage-load.md) <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |標準  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |標準  <br/> |
|その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド  <br/> |[IPersistMessage : IUnknown](ipersistmessageiunknown.md)インターフェイスのドキュメントで説明されているとおりに実装します。  <br/> |標準  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

