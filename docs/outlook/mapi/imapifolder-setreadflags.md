---
title: imapifoldersetreadflags
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
  
1つ以上のフォルダーのメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_lpmsglist_
  
> 順番設定またはクリアする読み取りフラグがあるメッセージまたはメッセージを識別する[entrylist](entrylist.md)構造体の配列へのポインター。 _lpmsglist_が NULL に設定されている場合は、すべてのフォルダーのメッセージの読み取りフラグが設定またはクリアされます。 
    
_uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで MESSAGE_DIALOG フラグが設定されていない場合は無視されます。 
    
_lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI の実装を使用して進行状況インジケーターを表示します。 MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
_ulFlags_
  
> 順番メッセージの読み取りフラグの設定と、閲覧レポートの処理を制御するフラグのビットマスク。 次のフラグを設定できます。
    
  - CLEAR_READ_FLAG: MSGFLAG_READ フラグを**PR_MESSAGE_FLAGS**でクリアし、閲覧レポートを送信しないようにする必要があります。 
        
  - CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDING フラグを**PR_MESSAGE_FLAGS**でクリアし、未開封のレポートを送信しないようにする必要があります。 
        
  - CLEAR_RN_PENDING: MSGFLAG_RN_PENDING フラグを**PR_MESSAGE_FLAGS**でクリアし、閲覧レポートを送信しないようにする必要があります。 
        
  - GENERATE_RECEIPT_ONLY: 読み取りレポートは、保留中の場合は送信されますが、MSGFLAG_READ フラグの状態は変更されません。
        
  - MAPI_DEFERRED_ERRORS: 操作が完了する前に、 **setreadflags**が正常に返されることを許可します。 
        
  - MESSAGE_DIALOG: 操作が進行している間、進行状況のインジケーターを表示します。
    
  - SUPPRESS_RECEIPT: 読み取りレポートが要求されている場合は、保留中の読み取りレポートを取り消す必要があります。この呼び出しは、メッセージの状態を未読から読み取りに変更します。 この呼び出しでメッセージの状態が変更されない場合、メッセージストアプロバイダーはこのフラグを無視できます。
    
## <a name="return-values"></a>戻り値

S_OK 
  
> 指定されたメッセージまたはメッセージの読み取りフラグが正常に設定またはクリアされました。
    
MAPI_E_NO_SUPPRESS 
  
> メッセージストアプロバイダーは、閲覧レポートの抑制をサポートしていません。
    
MAPI_E_INVALID_PARAMETER 
  
> 次のいずれかの互換性のないフラグの組み合わせが_ulflags_パラメーターで設定されています。 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのメッセージが正常に処理されませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>注釈

**imapifolder:: setreadflags**メソッドは、1つ以上のフォルダーのメッセージの**PR_MESSAGE_FLAGS**プロパティの MSGFLAG_READ フラグを設定またはクリアします。 MSGFLAG_READ フラグを設定すると、メッセージは開封済みとしてマークされます。これは、意図した受信者が実際にメッセージを読んでいることを示しているわけではありません。 
  
**setreadflags**は、閲覧レポートの送信も管理します。 
  
次の場合は、read フラグを変更できません。
  
- 存在しないメッセージ。
    
- 他の場所に移動されたメッセージ。
    
- 読み取り/書き込みアクセス許可で開いているメッセージ。
    
- 現在送信されているメッセージ。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

閲覧レポートの送信と、閲覧レポートを抑制する要求をサポートしないことを決定できます。 読み取りレポートを抑制しないようにするには、 **setreadflags**が_ulflags_パラメーターに set SUPPRESS_RECEIPT を指定して呼び出されたときに、MAPI_E_NO_SUPPRESS を返します。 
  
_lpmsglist_パラメーターが複数のメッセージをポイントしている場合は、メッセージごとに可能な限り完全に操作を実行します。 メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。 
  
_ulflags_パラメーターにどのフラグも設定されていない場合は、次のルールが適用されます。 
  
- MSGFLAG_READ が既に設定されている場合は、何も実行しません。
    
- MSGFLAG_READ が設定されていない場合は、直ちに設定して、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りレポートを送信します。
    
SUPPRESS_RECEIPT フラグが設定されている場合は、次のルールが適用されます。
  
- MSGFLAG_READ が既に設定されている場合は、何も実行しません。 
    
- MSGFLAG_READ が設定されていない場合は、設定し、保留中のすべての開封レポートを取り消します。
    
CLEAR_READ_FLAG フラグが設定されている場合は、各メッセージの**PR_MESSAGE_FLAGS**プロパティの MSGFLAG_READ フラグをオフにして、読み取りレポートを送信しないようにします。 
  
GENERATE_RECEIPT_ONLY フラグが設定されている場合は、保留中のすべての読み取りレポートを送信します。 MSGFLAG_READ を設定またはクリアしません。
  
SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合は、 **PR_READ_RECEIPT_REQUESTED**が設定されている場合は FALSE に設定し、閲覧レポートを送信しないようにします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件に当てはまることが予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**setreadflags**は、すべてのメッセージを正常に処理しました。  <br/> |S_OK  <br/> |
|**setreadflags**は、すべてのメッセージを正常に処理できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**setreadflags**を完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くすべてのエラー値  <br/> |
   
**setreadflags**が完了できない場合でも、作業が行われていないとは限りません。 **setreadflags**は、エラーが発生する前に、1つ以上のメッセージの MSGFLAG_READ フラグを設定またはクリアできた可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |cfolderdlg:: OnSetReadFlag  <br/> |mfcmapi は、指定されたメッセージに対して、 **imapifolder:: setreadflags**メソッドを使用して、手動で読み取り状態を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)  
- [PidTagReadReceiptRequested 標準プロパティ](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)  
- [エラー処理にマクロを使用する](using-macros-for-error-handling.md)

