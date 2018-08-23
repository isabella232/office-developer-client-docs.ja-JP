---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801114"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**適用対象**: Outlook 
  
指定されたメッセージのフォームが読み込まれます。
  
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
  
> [in]読み込まれるフォームのメッセージのサイトへのポインター。
    
 _pMessage_
  
> [in]フォームを読み込む必要があるメッセージへのポインター。
    
 _ulMessageStatus_
  
> [in]メッセージの状態に関する情報を提供するメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたクライアント定義またはプロバイダー定義のフラグのビットマスクです。
    
 _ulMessageFlags_
  
> [in]メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティからコピーして、フラグのビットマスクを提供するさらに、メッセージの状態に関する情報です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームが正常に読み込まれました。
    
## <a name="remarks"></a>注釈

フォームの閲覧者は、既存のメッセージのフォームをロードする**IPersistMessage::Load**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

 フォームが状態は、次のいずれかである場合にのみ、**ロード**が呼び出されます。 
  
- [初期化されていません](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
フォーム ビューアーは、フォームが他の状態では、**ロード**を呼び出し、メソッドは E_UNEXPECTED を返します。 
  
**負荷**に渡される 1 つは別の作業中のメッセージ、サイトへの参照は、フォームに場合、は、使用できなくするために元のサイトをリリースします。 _PMessageSite_と_pMessage_パラメーターからは、サイトのメッセージとメッセージへのポインターを格納し、その参照カウントをインクリメントするのには、両方のオブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。 
  
**AddRef**が完了したら、フォームに、 _ulMessageStatus_と_ulMessageFlags_のパラメーターのプロパティを格納します。 フォームを[通常](normal-state.md)の状態を表示するには、前に移行し、 [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出すことによって登録されている視聴者に通知します。 
  
エラーが発生しない場合は、S_OK を返します。 
  
## <a name="see-also"></a>関連項目



[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Uninitialized 状態](uninitialized-state.md)
  
[HandsOffAfterSave 状態](handsoffaftersave-state.md)
  
[HandsOffFromNormal 状態](handsofffromnormal-state.md)
  
[フォームの状態](form-states.md)


[機能として](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

