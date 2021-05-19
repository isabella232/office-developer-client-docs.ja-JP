---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418639"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のフォルダー内のメッセージに関連付けられている状態を取得します (たとえば、そのメッセージが削除のマークが付けられているかどうかなど)。
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]状態が取得されたメッセージのエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulMessageStatus_
  
> [out]メッセージの状態を示すフラグのビットマスクへのポインター。 ビット 0 ~ 15 は予約済みで、ゼロである必要があります。ビット 16 ~ 31 は、実装固有の使用に使用できます。 次のフラグを設定できます。
    
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
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの状態が正常に取得されました。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::GetMessageStatus** メソッドは、メッセージの状態を返します。 メッセージの状態は、メッセージのプロパティ ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md) **)** PR_MSG_STATUSに格納されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージの状態ビットの設定方法、クリア方法、および使用方法は、実装によって完全に異なりますが、ビット 0 ~ 15 は予約済みで、ゼロである必要があります。 IPM サブツリーにメッセージを格納する場合、MAPI は IPM クライアントで使用するためにビット 16 ~ 31 を予約します。 他のサブツリーにメッセージを格納する場合は、ビット 16 ~ 31 を独自の目的で使用できます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI は **IMAPIFolder::GetMessageStatus** メソッドを使用して、表示する次のメッセージの状態を取得します。  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal と OpenMessageModal  <br/> |MFCMAPI は **IMAPIFolder::GetMessageStatus** メソッドを使用して、表示するメッセージの状態を取得してフォーム ビューアーに渡します。これは CMyMAPIFormViewer または [IMAPISession::ShowForm](imapisession-showform.md)です。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

