---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 88185efea344844016547d0844277de6e0d661db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578319"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**適用されます**: Outlook 2013 |Outlook 2016 
  
設定または、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに 1 つまたは複数のフォルダーのメッセージでは、MSGFLAG_READ フラグをクリアし、リードのレポートの送信を管理します。 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_lpMsgList_
  
> [in]メッセージのフラグをオンまたはオフに読み取られたメッセージを識別する[ENTRYLIST](entrylist.md)構造体の配列へのポインター。 _LpMsgList_は、NULL に設定されている場合、読み取りはすべてフォルダーのメッセージを設定またはクリアのフラグです。 
    
_ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターに MESSAGE_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。 
    
_lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI の実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
_ulFlags_
  
> [in]メッセージの読み取りフラグの設定の処理を制御するフラグのビットマスクは、レポートをお読みください。 次のフラグを設定することができます。
    
  - CLEAR_READ_FLAG: **PR_MESSAGE_FLAGS**に MSGFLAG_READ フラグをクリアする必要があり、リードのレポートは送信されませんする必要があります。 
        
  - CLEAR_NRN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_NRN_PENDING フラグをクリアする必要があり、未読のレポートを送信しない必要があります。 
        
  - CLEAR_RN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_RN_PENDING フラグをクリアする必要があり、リードのレポートは送信されませんする必要があります。 
        
  - GENERATE_RECEIPT_ONLY: 1 つは、保留中が存在しないはずの MSGFLAG_READ フラグの状態の変更は、リードのレポートを送信してください。
        
  - MAPI_DEFERRED_ERRORS: 正常に完了可能性がありますが、操作を完了する前にするには**SetReadFlags**を使用できます。 
        
  - MESSAGE_DIALOG: は、操作の進行中に進行状況のインジケーターを表示します。
    
  - SUPPRESS_RECEIPT: 要求された読み取りのレポートと、この呼び出しからの読み取りに未読のメッセージの状態を変更する場合は、保留中の読み取りレポートをキャンセルするか。 この呼び出しで、メッセージの状態が変化しない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。
    
## <a name="return-values"></a>戻り値

S_OK 
  
> 読み取り、指定したメッセージまたはメッセージのフラグを設定またはクリアに成功しました。
    
MAPI_E_NO_SUPPRESS 
  
> メッセージ ストア プロバイダーは、レポートの読み込みの抑制をサポートしていません。
    
MAPI_E_INVALID_PARAMETER 
  
> _UlFlags_パラメーターで次の互換性のないフラグの組み合わせのいずれかに設定されます。 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、すべてのメッセージを正常に処理されました。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::SetReadFlags**メソッドを設定またはフォルダーのメッセージの 1 つ以上の**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_READ フラグをクリアします。 開封は必ずしも、目的の受信者がメッセージを読むには実際にメッセージをマークする MSGFLAG_READ フラグを設定します。 
  
**SetReadFlags**リードのレポートの送信を管理します。 
  
読み取りフラグは、次の変更ことはできません。
  
- 存在しないメッセージです。
    
- されているメッセージは、他の場所を移動します。
    
- 読み取り/書き込み権限で開かれているメッセージです。
    
- 現在送信されるメッセージです。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

レポートの読み取りと読み取りのレポートを非表示にする要求の送信をサポートしないようにすることができます。 リードのレポートを抑制することを避けるため、 _ulFlags_パラメーターを設定する SUPPRESS_RECEIPT と**SetReadFlags**が呼び出されたときに MAPI_E_NO_SUPPRESS を返します。 
  
_LpMsgList_パラメーターは、複数のメッセージをポイントしているときに、できるだけ完全に各メッセージの操作を実行します。 メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。 
  
_UlFlags_パラメーターでは、どのフラグが設定されている場合は、次の規則が適用されます。 
  
- MSGFLAG_READ は既に設定されている場合は機能しません。
    
- MSGFLAG_READ が設定されていない場合それをすぐに設定し、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りのレポートを送信します。
    
SUPPRESS_RECEIPT フラグが設定されている場合は、次の規則が適用されます。
  
- MSGFLAG_READ は既に設定されている場合は機能しません。 
    
- MSGFLAG_READ が設定されていない場合は、それを設定し、保留中の読み取りのレポートをキャンセルします。
    
CLEAR_READ_FLAG フラグを設定すると各メッセージの**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_READ フラグをオフに、読み取りのレポートを送信しません。 
  
GENERATE_RECEIPT_ONLY フラグが設定されている場合は、すべての保留中の読み取りレポートを送信します。 MSGFLAG_READ を設定したりクリアの操作を行います。
  
SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合設定**PR_READ_RECEIPT_REQUESTED** FALSE に設定されている場合、読み取りのレポートを送信しません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

次の条件下で、これらの戻り値を期待してください。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**SetReadFlags**では、すべてのメッセージが正常に処理します。  <br/> |S_OK  <br/> |
|**SetReadFlags**は、すべてのメッセージを正常に処理できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags**は完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くエラー値  <br/> |
   
**SetReadFlags**が完了することではない場合と仮定しないでその作業は実行されませんでした。 **SetReadFlags**を設定または 1 つまたは複数のメッセージのエラーが発生する前に MSGFLAG_READ フラグをオフにすることされている可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI では、 **IMAPIFolder::SetReadFlags**メソッドを使用して、指定されたメッセージの読み取り状態を手動で設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)  
- [PidTagReadReceiptRequested 標準プロパティ](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)  
- [エラー処理のためのマクロの使用](using-macros-for-error-handling.md)

