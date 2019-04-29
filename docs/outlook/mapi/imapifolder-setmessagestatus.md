---
title: imapifoldersetmessagestatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417274"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージに関連付けられている状態を設定します (メッセージに削除のマークが付いているかどうかなど)。
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番状態が設定されているメッセージのエントリ id へのポインター。
    
 _ulnewstatus_
  
> 順番割り当てられる新しい状態。 
    
 _ulnewstatusmask_
  
> 順番新しい状態に適用されるフラグのビットマスク。設定するフラグを示します。 次のフラグを設定できます。
    
MSGSTATUS_DELMARKED 
  
> メッセージは削除対象としてマークされています。
    
MSGSTATUS_HIDDEN 
  
> メッセージは表示されません。
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージは強調表示されます。
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージがリモートメッセージストアで削除対象としてマークされ、ローカルクライアントにダウンロードされていません。
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモートメッセージストアからローカルクライアントにダウンロードするようにマークされています。
    
MSGSTATUS_TAGGED 
  
> メッセージには、クライアント定義の目的のタグが付けられています。
    
 _lpuloldstatus_
  
> 読み上げメッセージの以前の状態へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの状態が正常に設定されました。
    
## <a name="remarks"></a>注釈

**imapifolder:: setmessagestatus**メソッドは、メッセージの状態を**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに格納されている値に設定します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージ状態のビットがどのように設定、クリア、使用されるかは、実装に完全に依存します。ただし、ビット 0 ~ 15 は予約されており、0である必要があります。 
  
リモートトランスポートプロバイダーのこのメソッドの実装は、ここで説明するセマンティクスに従う必要があります。 特別な考慮事項はありません。 クライアントはこのメソッドを使用して、MSGSTATUS_REMOTE_DOWNLOAD および MSGSTATUS_REMOTE_DELETE ビットを設定し、リモートメッセージストアから特定のメッセージをダウンロードまたは削除することを示します。 リモートトランスポートプロバイダーは、関連する[imapifolder:: getmessagestatus](imapifolder-getmessagestatus.md)メソッドを実装する必要はありません。 クライアントは、フォルダーの contents テーブルを調べて、メッセージの状態を確認する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの**PR_MSG_STATUS**プロパティを使用して、他のクライアントとのメッセージロックアウト操作をネゴシエートできます。 ロックアウトビットとしてビットを指定します。 ロックアウトビットが設定されているかどうかを確認するには、 _lpuloldstatus_パラメーターのメッセージの状態について前の値を調べます。 _ulnewstatus_パラメーターの他のビットを使用して、ロックアウトビットを妨げることなくメッセージの状態を追跡します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

