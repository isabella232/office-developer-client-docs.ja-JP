---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 23b486a91701a317f23b6dd1f0018db115f369c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579769"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したメッセージのフォームを読み込む。
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>パラメーター

 _pMessageSite_
  
> [in]フォームを読み込むメッセージ サイトへのポインター。
    
 _pMessage_
  
> [in]フォームを読み込むメッセージへのポインター。
    
 _ulMessageStatus_
  
> [in]メッセージの状態に関する情報を提供する、メッセージ **の PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされた、クライアント定義フラグまたはプロバイダー定義フラグのビットマスク。
    
 _ulMessageFlags_
  
> [in]メッセージの状態に関する詳細な情報を提供する、メッセージの **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に読み込まれた。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **、IPersistMessage::Load** メソッドを呼び出して、既存のメッセージのフォームを読み込む。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

 **読** み込みは、フォームが次のいずれかの状態にある場合にのみ呼び出されます。 
  
- [初期化されていません](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
フォーム ビューアーが他の状態 **にある間** に Load を呼び出した場合、メソッドはユーザーをE_UNEXPECTED。 
  
フォームに Load に渡されるメッセージ サイト以外のアクティブなメッセージ サイトへの参照がある場合は、元のサイトが使用されなくなったため、元のサイトを解放します。 _pMessageSite_ パラメーターと _pMessage_ パラメーターからメッセージ サイトへのポインターとメッセージを格納し、両方のオブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、参照カウントを増やします。 
  
**AddRef が** 完了したら _、ulMessageStatus_ パラメーターと _ulMessageFlags_ パラメーターのプロパティをフォームに格納します。 フォームを表示する前 [にフォーム](normal-state.md) を標準状態に切り替え [、IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) メソッドを呼び出して登録された閲覧者に通知します。 
  
エラーが発生しない場合は、S_OK。 
  
## <a name="see-also"></a>関連項目



[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[初期化されていない状態](uninitialized-state.md)
  
[HandsOffAfterSave 状態](handsoffaftersave-state.md)
  
[HandsOffFromNormal State](handsofffromnormal-state.md)
  
[フォームの状態](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

