---
title: IMAPIFolderSetMessageStatus
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
  
メッセージに関連付けられた状態を設定します (たとえば、そのメッセージが削除のマークが付けられているかどうかなど)。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]状態が設定されているメッセージのエントリ識別子へのポインター。
    
 _ulNewStatus_
  
> [in]割り当てる新しい状態。 
    
 _ulNewStatusMask_
  
> [in]新しい状態に適用され、設定するフラグを示すフラグのビットマスク。 次のフラグを設定できます。
    
MSGSTATUS_DELMARKED 
  
> メッセージが削除のマークが付いている。
    
MSGSTATUS_HIDDEN 
  
> メッセージは表示されません。
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージが強調表示されます。
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージは、ローカル クライアントにダウンロードせずにリモート メッセージ ストアで削除のマークが付けされています。
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロードするマークが付けされています。
    
MSGSTATUS_TAGGED 
  
> メッセージは、クライアント定義の目的でタグ付けされています。
    
 _lpulOldStatus_
  
> [out]メッセージの以前の状態へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの状態が正常に設定されました。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::SetMessageStatus** メソッドは、メッセージの状態を、メッセージ のプロパティ **(** [PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) PR_MSG_STATUSに格納されている値に設定します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージの状態ビットの設定方法、クリア方法、および使用方法は、実装によって完全に異なりますが、ビット 0 ~ 15 は予約済みで、ゼロである必要があります。 
  
リモート トランスポート プロバイダーによるこのメソッドの実装は、ここで説明するセマンティクスに従う必要があります。 特別な考慮事項はありません。 クライアントは、このメソッドを使用して、MSGSTATUS_REMOTE_DOWNLOAD および MSGSTATUS_REMOTE_DELETE ビットを設定して、特定のメッセージをリモート メッセージ ストアからダウンロードまたは削除する必要があるかどうかを示します。 リモート トランスポート プロバイダーは、関連する [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) メソッドを実装する必要があります。 クライアントは、メッセージの状態を決定するためにフォルダーのコンテンツ テーブルを参照する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの **PR_MSG_STATUS** プロパティを使用して、他のクライアントとメッセージロックアウト操作をネゴシエートできます。 ビットをロックアウト ビットとして指定します。 ロックアウト ビットが設定されているかどうかを確認するには  _、lpulOldStatus_ パラメーターでメッセージの状態について前の値を調べてください。 _ulNewStatus_ パラメーターの他のビットを使用して、ロックアウト ビットを妨げることなくメッセージの状態を追跡します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

