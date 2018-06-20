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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fcca6a7e8fa70a2df9042e8b3c2b28825cee9a7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800501"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**適用されます**: Outlook 
  
(たとえば、あるかどうかそのメッセージは削除対象としてマーク) は、メッセージに関連付けられたステータスを設定します。
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]ステータスが設定されて、メッセージのエントリの識別子へのポインター。
    
 _ulNewStatus_
  
> [in]割り当てられる新しい状態です。 
    
 _ulNewStatusMask_
  
> [in]新しい状態に適用され、フラグを設定することを示しますフラグのビットマスク。 次のフラグを設定することができます。
    
MSGSTATUS_DELMARKED 
  
> メッセージは、削除対象としてマークされています。
    
MSGSTATUS_HIDDEN 
  
> メッセージは表示しません。
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージが表示されるが強調表示されています。
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージは、ローカル クライアントにダウンロードすることがなくリモート メッセージ ストアを削除対象としてマークされています。
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロード用にマークされています。
    
MSGSTATUS_TAGGED 
  
> クライアント定義の目的は、メッセージをタグ付けされました。
    
 _lpulOldStatus_
  
> [out]メッセージの前の状態へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージの状態が正常に設定されました。
    
## <a name="remarks"></a>備考

**IMAPIFolder::SetMessageStatus**メソッドは、メッセージの状態を**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティに格納されている値に設定します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

メッセージのステータス ビットを設定、オフになっていると使用する方法によって異なります完全に、実装がビット 0 ~ 15 は予約されており、0 にする必要があります。 
  
このメソッドをリモート トランスポート プロバイダーの実装は、ここで説明するセマンティクスに従う必要があります。 特別な考慮事項はありません。 クライアントは、特定のメッセージがダウンロードするか、リモート メッセージ ストアから削除するのにことを示す MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE のビットを設定するのには、このメソッドを使用します。 リモート トランスポート プロバイダーは、関連する[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)メソッドを実装するためにはありません。 クライアントは、メッセージのステータスを確認するのにはフォルダーの内容のテーブルで検索する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの**PR_MSG_STATUS**プロパティを使用するには他のクライアントとメッセージのロックアウト操作をネゴシエートします。 ロックアウト ビットとビットを指定します。 ロックアウト ビットが設定されているかどうかを確認するのには、 _lpulOldStatus_パラメーターでメッセージの状態の以前の値を確認します。 _UlNewStatus_パラメーターで他のビットを使用して、ロックアウト ビットに干渉することがなくメッセージのステータスを追跡します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[PidTagMessageStatus の標準的なプロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)

