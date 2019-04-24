---
title: noscribble 状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326202"
---
# <a name="noscribble-state"></a>noscribble 状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
noscribble 状態は、メッセージの変更が保存されていることを示します。 form オブジェクトのユーザーインターフェイスに格納されている値は、クライアントアプリケーションによってフォームオブジェクトの[IPersistMessage:: Save](ipersistmessage-save.md)メソッドが呼び出されたときに実際に保存されます。 次の表は、noscribble 状態から許可される遷移を示しています。 
  
|IPersistMessage * * メソッド * *|**Action**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)(_pmessage = =_ NULL)  <br/> |フォームが noscribble 状態に入り、メッセージが変更されたという[IPersistMessage:: Save](ipersistmessage-save.md)呼び出しで、 _fsameasload_フラグが TRUE に設定されている場合は、変更を保存済みとして内部的にマークして、 [IMAPIViewAdviseSink:: onsaved](imapiviewadvisesink-onsaved.md)を呼び出します。手段.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage:: SaveCompleted**(_pmessage! =_ NULL)  <br/> |[IPersistMessage::](ipersistmessage-handsoffmessage.md)配布 (OLE [IPersistStorage:: soffstorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)メソッドと同様の) メソッドを呼び出します。その後に通常の**SaveCompleted**アクションが続きます。 **SaveCompleted**が正常に終了した場合は、通常の状態を入力します。 それ以外の場合は、[[保存](handsoffaftersave-state.md)の状態] を入力します。  <br/> |Normal または標準の保存  <br/> |
|**「soffmessage」** <br/> |埋め込まれ**** たメッセージに対して、または ole **IPersistStorage:: 配布用**の ole オブジェクトに対して、配布のために、このメソッドを再帰的に呼び出します。 メッセージオブジェクトおよび埋め込まれたメッセージまたはオブジェクトを解放します。  <br/> |HandsOffAfterSave  <br/> |
|**Save**、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)、または[IPersistMessage:: Load](ipersistmessage-load.md) <br/> |最後のエラーをに設定し、E_UNEXPECTED を返します。  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |直前のエラーを返します。  <br/> |NoScribble  <br/> |
|その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド  <br/> |最後のエラーをに設定し、E_UNEXPECTED を返します。  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

