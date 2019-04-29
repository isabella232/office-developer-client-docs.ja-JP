---
title: imapifoldergetmessagestatus
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
  
特定のフォルダー内のメッセージに関連付けられている状態を取得します (たとえば、そのメッセージに削除のマークが付いているかどうか)。
  
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番状態が取得されるメッセージのエントリ id へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lアウト messagestatus_
  
> 読み上げメッセージの状態を示すフラグのビットマスクへのポインターへのポインター。 ビット 0 ~ 15 は予約されており、0である必要があります。bits 16 ~ 31 は実装固有の用途に使用できます。 次のフラグを設定できます。
    
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
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの状態が正常に取得されました。
    
## <a name="remarks"></a>注釈

**imapifolder:: getmessagestatus**メソッドは、メッセージの状態を返します。 メッセージの状態は、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに格納されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージ状態のビットがどのように設定、クリア、使用されるかは、実装に完全に依存します。ただし、ビット 0 ~ 15 は予約されており、0である必要があります。 メッセージを ipm サブツリーに格納する場合、MAPI は、ipm クライアントによって使用されるビット 16 ~ 31 を予約します。 他のサブツリーにメッセージを格納する場合は、独自の用途にビット16から31を使用できます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: GetNextMessage  <br/> |mfcmapi は、 **imapifolder:: getmessagestatus**メソッドを使用して、次に表示されるメッセージの状態を取得します。  <br/> |
|MAPIFormFunctions  <br/> |openmessagenonmodal および openmessagemodal  <br/> |mfcmapi は、 **imapifolder:: getmessagestatus**メソッドを使用して、フォームビューアーに渡すために表示されるメッセージの状態を取得します。これは、cmymapiformviewer または[imapifolder:: showform](imapisession-showform.md)のいずれかです。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

