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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317130"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したメッセージのフォームを読み込みます。
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>パラメーター

 _pメッセージ ite_
  
> 順番フォームを読み込むためのメッセージサイトへのポインター。
    
 _pmessage_
  
> 順番フォームを読み込むメッセージへのポインター。
    
 _ulmessagestatus_
  
> 順番メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーし、メッセージの状態に関する情報を提供する、クライアント定義またはプロバイダー定義のフラグのビットマスク。
    
 _ulmessageflags_
  
> 順番メッセージの状態に関する詳細情報を提供するフラグのビットマスク。メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に読み込まれました。
    
## <a name="remarks"></a>解説

フォームビューアーは**IPersistMessage:: load**メソッドを呼び出して、既存のメッセージのフォームを読み込みます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

 **Load**は、フォームが次のいずれかの状態にある場合にのみ呼び出されます。 
  
- [初期化されていません](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
フォームが他の状態にあるときにフォームビューアーが**Load**を呼び出すと、メソッドは E_UNEXPECTED を返します。 
  
フォームに、**読み込み**に渡されたものとは異なるアクティブなメッセージサイトへの参照がある場合は、そのサイトが使用されなくなったため、元のサイトを解放します。 メッセージサイトおよびメッセージへのポインターを pメッセージパラメーター __ と_pmessage_パラメーターから格納し、両方のオブジェクト ' [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して参照カウントをインクリメントします。 
  
**AddRef**が完了したら、 _ulmessagestatus_パラメーターと_ulmessagestatus_パラメーターのプロパティをフォームに格納します。 フォームを表示する前に[通常](normal-state.md)の状態に移行し、 [IMAPIViewAdviseSink:: onnewmessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出して、登録されているビューアーに通知します。 
  
エラーが発生しない場合は、S_OK を返します。 
  
## <a name="see-also"></a>関連項目



[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[未初期化状態](uninitialized-state.md)
  
[保存の状態を処理する](handsoffaftersave-state.md)
  
[標準の状態](handsofffromnormal-state.md)
  
[フォームの状態](form-states.md)


[IPersistStorage:: Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream:: Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile:: Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

