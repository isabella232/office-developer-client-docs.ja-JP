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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406914"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**適用対象**: Outlook 2013 | Outlook 2016 
  
**1** つ以上のフォルダーのメッセージの PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、読み取りレポートの送信を管理します。 
  
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
  
> [in]設定またはクリアする読み取りフラグを持つメッセージまたはメッセージを識別する [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。 _lpMsgList が_ NULL に設定されている場合、フォルダーのすべてのメッセージの読み取りフラグが設定またはクリアされます。 
    
_ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター MESSAGE_DIALOGフラグが設定されていない限り、無視されます。 
    
_lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI の実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。
    
_ulFlags_
  
> [in]メッセージの読み取りフラグの設定と読み取りレポートの処理を制御するフラグのビットマスク。 次のフラグを設定できます。
    
  - CLEAR_READ_FLAG: MSGFLAG_READフラグは、PR_MESSAGE_FLAGSでクリアする必要があります。また、読み取りレポートを送信する必要があります。 
        
  - CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDINGフラグは、PR_MESSAGE_FLAGSでクリアする必要があります。未読レポートは送信されません。 
        
  - CLEAR_RN_PENDING: MSGFLAG_RN_PENDINGのチェック ボックスをオフPR_MESSAGE_FLAGS、読み取 **り** レポートを送信する必要があります。 
        
  - GENERATE_RECEIPT_ONLY: 保留中の場合は読み取りレポートを送信する必要がありますが、このフラグの状態に変更MSGFLAG_READがあります。
        
  - MAPI_DEFERRED_ERRORS: 操作が完了する前に **、SetReadFlags** を正常に返します。 
        
  - MESSAGE_DIALOG: 操作の実行中に進行状況インジケーターを表示します。
    
  - SUPPRESS_RECEIPT: 読み取りレポートが要求され、この呼び出しによってメッセージの状態が未読から読み取りに変更された場合は、保留中の読み取りレポートを取り消す必要があります。 この呼び出しでメッセージの状態が変更されない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。
    
## <a name="return-values"></a>戻り値

S_OK 
  
> 指定したメッセージまたはメッセージの読み取りフラグが正常に設定またはクリアされました。
    
MAPI_E_NO_SUPPRESS 
  
> メッセージ ストア プロバイダーは、読み取りレポートの抑制をサポートしていない。
    
MAPI_E_INVALID_PARAMETER 
  
> ulFlags パラメーターでは、フラグの互換性のない組み合  _わせの 1 つが設定_ されています。 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのメッセージが正常に処理されたというのではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::SetReadFlags** メソッドは、1 つ以上のフォルダーのメッセージの PR_MESSAGE_FLAGS プロパティの **MSGFLAG_READ** フラグを設定またはクリアします。 メッセージフラグMSGFLAG_READ設定すると、メッセージは読み取りとしてマークされます。これは、必ずしも意図した受信者が実際にメッセージを読み取ったとは限りません。 
  
**SetReadFlags は、** 読み取りレポートの送信も管理します。 
  
次の場合は、読み取りフラグを変更できません。
  
- 存在しないメッセージ。
    
- 他の場所に移動されたメッセージ。
    
- 読み取り/書き込み権限で開いているメッセージ。
    
- 現在送信されているメッセージ。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

読み取りレポートの送信と、読み取りレポートを抑制する要求をサポートしない場合があります。 読み取りレポートを抑制しないようにするには _、ulFlags_ パラメーター MAPI_E_NO_SUPPRESS Set で **SetReadFlags** が呼び出SUPPRESS_RECEIPTを返します。 
  
_lpMsgList パラメーターが_ 複数のメッセージをポイントする場合は、メッセージごとに可能な限り完全に操作を実行します。 メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。 
  
_ulFlags_ パラメーターにフラグが設定されない場合は、次の規則が適用されます。 
  
- 既MSGFLAG_READ設定されている場合は、何も行いません。
    
- このMSGFLAG_READ設定されていない場合は、すぐに設定し **、PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りレポートを送信します。
    
このフラグSUPPRESS_RECEIPT設定すると、次のルールが適用されます。
  
- 既MSGFLAG_READ設定されている場合は、何も行いません。 
    
- このMSGFLAG_READ設定されていない場合は、設定し、保留中の読み取りレポートを取り消します。
    
このフラグCLEAR_READ_FLAG設定されている場合は、各メッセージの MSGFLAG_READ プロパティの PR_MESSAGE_FLAGS フラグをクリアし、読み取りレポートを送信しない。 
  
このフラグGENERATE_RECEIPT_ONLY設定されている場合は、保留中の読み取りレポートを送信します。 設定または削除を行MSGFLAG_READ。
  
SUPPRESS_RECEIPTフラグと GENERATE_RECEIPT_ONLY フラグの両方が設定されている場合は、PR_READ_RECEIPT_REQUESTEDを FALSE に設定し、読み取りレポートを送信しない。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件下で期待してください。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**SetReadFlags は** 、すべてのメッセージを正常に処理しました。  <br/> |S_OK  <br/> |
|**SetReadFlags は** 、すべてのメッセージを正常に処理できなかった。  <br/> |MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** を完了できません。  <br/> |エラー以外のエラー MAPI_E_NOT_FOUND  <br/> |
   
**SetReadFlags を** 完了できない場合は、作業が完了していないと想定しません。 **エラーが発生する前に、SetReadFlags** が 1 つ以上のメッセージMSGFLAG_READフラグを設定またはクリアできた可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI は **IMAPIFolder::SetReadFlags** メソッドを使用して、指定されたメッセージの読み取り状態を手動で設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)  
- [PidTagReadReceiptRequested 標準プロパティ](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)  
- [エラー処理にマクロを使用する](using-macros-for-error-handling.md)

