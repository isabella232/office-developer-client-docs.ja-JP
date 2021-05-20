---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439871"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの MSGFLAG_READ ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ **PR_MESSAGE_FLAGS** フラグを設定またはクリアし、読み取りレポートの送信を管理します。
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> [in]メッセージの読み取りフラグの設定 **(PR_MESSAGE_FLAGS** プロパティのメッセージの MSGFLAG_READ フラグ、および読み取りレポートの処理を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
  - CLEAR_READ_FLAG: MSGFLAG_READフラグは、PR_MESSAGE_FLAGSでクリアし、読み取 **り** レポートを送信する必要はありません。 
      
  - CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDINGフラグは、PR_MESSAGE_FLAGSでクリアする必要があります。読み取り以外のレポートを送信する必要があります。 
      
  - CLEAR_RN_PENDING: MSGFLAG_RN_PENDINGフラグは、PR_MESSAGE_FLAGSでクリアし、読み取 **り** レポートを送信する必要はありません。 
      
  - GENERATE_RECEIPT_ONLY: 保留中の場合は読み取りレポートを送信する必要がありますが、このフラグの状態に変更MSGFLAG_READがあります。
      
  - MAPI_DEFERRED_ERRORS: 操作が完了する前に **、SetReadFlag** を正常に返します。 
      
  - SUPPRESS_RECEIPT: 読み取りレポートが要求され、この呼び出しによってメッセージの状態が未読から読み取りに変更された場合は、保留中の読み取りレポートを取り消す必要があります。 この呼び出しでメッセージの状態が変更されない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの読み取りフラグが正常に設定またはクリアされました。
    
MAPI_E_NO_SUPPRESS 
  
> メッセージ ストア プロバイダーは、読み取りレポートの抑制をサポートしていない。
    
MAPI_E_INVALID_PARAMETER 
  
> ulFlags パラメーターには、次のいずれかのフラグの組  _み合わせが設定_ されています。 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>注釈

**IMessage::SetReadFlag** メソッドは **、PR_MESSAGE_FLAGS** プロパティでメッセージの MSGFLAG_READ フラグを設定またはクリアし [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出してメッセージを保存します。 MSGFLAG_READフラグを設定すると、メッセージが読み取りされたとマークされます。これは、意図した受信者が実際にメッセージを読み取ったとは限りません。 
  
**SetReadFlags は、** 読み取りレポートの送信も管理します。 読み取りレポートは、送信者が要求した場合にのみ送信されます。 
  
読み取りフラグは、次の場合に変更できません。
  
- 存在しないメッセージ。
    
- 他の場所に移動されたメッセージ。
    
- 読み取り/書き込み権限で開いているメッセージ。
    
- 現在送信されているメッセージ。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

_ulFlags_ パラメーターにフラグが設定されない場合は、次の規則が適用されます。 
  
- 既MSGFLAG_READ設定されている場合は、何も行いません。
    
- このMSGFLAG_READ設定されていない場合は、PR_READ_RECEIPT_REQUESTED **(** [PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、それを設定し、保留中の読み取りレポートを送信します。
    
SUPPRESS_RECEIPT フラグと GENERATE_RECEIPT_ONLY フラグの両方が設定されている場合、PR_READ_RECEIPT_REQUESTED ビットを設定するとクリアされ、読み取りレポートは送信されません。
  
このフラグSUPPRESS_RECEIPT設定されている場合は、次の条件を実行します。
  
- 既MSGFLAG_READ設定されている場合は、何も行いません。 
    
- このMSGFLAG_READ設定されていない場合は、設定し、保留中の読み取りレポートを取り消します。
    
このフラグCLEAR_READ_FLAG設定されている場合は、各メッセージの MSGFLAG_READ プロパティの PR_MESSAGE_FLAGS フラグをクリアし、読み取りレポートを送信しない。 
  
このフラグGENERATE_RECEIPT_ONLY設定されている場合は、保留中の読み取りレポートを送信します。 設定または削除を行MSGFLAG_READ。
  
SUPPRESS_RECEIPT フラグと GENERATE_RECEIPT_ONLY フラグの両方が設定されている場合は、PR_READ_RECEIPT_REQUESTED プロパティを FALSE に設定し、読み取りレポートを送信しない場合は FALSE に設定します。
  
特定の条件下で読み取りレポートの生成を抑制することで、レポートの動作を最適化できます。 ただし、レポートの抑制をサポートしていない場合に、クライアントが **setReadFlag** を呼び出し、SUPPRESS_RECEIPTフラグを設定した場合は、MAPI_E_NO_SUPPRESS。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI は **、IMessage::SetReadFlag** メソッドを使用して、選択したメッセージに対して読み取りフラグを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

