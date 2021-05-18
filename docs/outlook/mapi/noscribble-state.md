---
title: NoScribble 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326202"
---
# <a name="noscribble-state"></a>NoScribble 状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
NoScribble 状態は、メッセージに対する変更が保存されている状態を示します。 フォーム オブジェクトのユーザー インターフェイスに格納されている値の実際の保存は、フォーム オブジェクトの [IPersistMessage::Save](ipersistmessage-save.md) メソッドがクライアント アプリケーションによって呼び出された場合に発生します。 次の表では、NoScribble 状態からの許可された移行について説明します。 
  
|IPersistMessage** メソッド**|**Action**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |フォームが NoScribble 状態に入り、メッセージが変更された [IPersistMessage::Save](ipersistmessage-save.md)呼び出しで _fSameAsLoad_ フラグが TRUE の場合は、内部的に変更を保存済みとしてマークし [、IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)メソッドを呼び出します。  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッド (OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドと同様) を呼び出し、その後に通常の **SaveCompleted** アクションを実行します。 **SaveCompleted が成功した** 場合は、Normal 状態を入力します。 それ以外の場合は [、HandsOffAfterSave 状態を入力](handsoffaftersave-state.md) します。  <br/> |Normal または HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |埋め込みメッセージ **の HandsOffMessage** メソッド、または埋め込み OLE オブジェクトの OLE **IPersistStorage::HandsOffStorage** メソッドを再帰的に呼び出します。 メッセージ オブジェクトと埋め込みメッセージまたはオブジェクトを解放します。  <br/> |HandsOffAfterSave  <br/> |
|**Save** [、IPersistMessage::InitNew、](ipersistmessage-initnew.md)[または IPersistMessage::Load](ipersistmessage-load.md) <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |NoScribble  <br/> |
|その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド  <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

