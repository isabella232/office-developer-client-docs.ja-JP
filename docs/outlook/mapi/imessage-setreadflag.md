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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800896"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**適用対象**: Outlook 
  
設定し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに MSGFLAG_READ フラグをクリアまたはリードのレポートの送信を管理します。
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

_ulFlags_
  
> [in]メッセージの読み取りの設定を制御するフラグのビットマスクのフラグは、その**PR_MESSAGE_FLAGS**プロパティは、読み取りのレポートの処理に MSGFLAG_READ フラグをメッセージの。 次のフラグを設定することができます。 
    
  - CLEAR_READ_FLAG: **PR_MESSAGE_FLAGS**に MSGFLAG_READ フラグをクリアする必要があり、リードのレポートを送信しません。 
      
  - CLEAR_NRN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_NRN_PENDING フラグをクリアする必要があり、未開封レポートを送信しない必要があります。 
      
  - CLEAR_RN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_RN_PENDING フラグをクリアする必要があり、リードのレポートを送信しません。 
      
  - GENERATE_RECEIPT_ONLY: 1 つは、保留中が存在しないはずの MSGFLAG_READ フラグの状態の変更は、リードのレポートを送信してください。
      
  - MAPI_DEFERRED_ERRORS: 正常に完了可能性がありますが、操作を完了する前にするには**SetReadFlag**を使用できます。 
      
  - SUPPRESS_RECEIPT: 要求された読み取りのレポートと、この呼び出しからの読み取りに未読のメッセージの状態を変更する場合は、保留中の読み取りレポートをキャンセルするか。 この呼び出しで、メッセージの状態が変化しない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 読み取りフラグは正常に設定またはクリアされました。
    
MAPI_E_NO_SUPPRESS 
  
> メッセージ ストア プロバイダーは、レポートの読み込みの抑制をサポートしていません。
    
MAPI_E_INVALID_PARAMETER 
  
> _UlFlags_パラメーターで次のフラグの組み合わせのいずれかに設定されます。 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>注釈

**IMessage::SetReadFlag**メソッドを設定または、 **PR_MESSAGE_FLAGS**プロパティと、メッセージを保存するのには[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の呼び出しでのメッセージの MSGFLAG_READ フラグをクリアします。 MSGFLAG_READ フラグを設定は、必ずしも目的の受信者がメッセージを読むには実際には、読み取りとメッセージをマークします。 
  
**SetReadFlags**リードのレポートの送信を管理します。 いずれかの送信者が要求された場合のみ、読み取りのレポートが送信されます。 
  
読み取りフラグを変更することはできません。
  
- 存在しないメッセージです。
    
- されているメッセージは、他の場所を移動します。
    
- 読み取り/書き込み権限で開かれているメッセージです。
    
- 現在送信されるメッセージです。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

_UlFlags_パラメーターでは、どのフラグが設定されている場合は、次の規則が適用されます。 
  
- MSGFLAG_READ は既に設定されている場合は機能しません。
    
- MSGFLAG_READ が設定されていない場合は、それを設定し、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りのレポートを送信します。
    
SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合、PR_READ_RECEIPT_REQUESTED ビットの場合はこのオプションを設定すると、クリアする必要があり、リードのレポートは送信されませんする必要があります。
  
SUPPRESS_RECEIPT フラグを設定するとします。
  
- MSGFLAG_READ は既に設定されている場合は機能しません。 
    
- MSGFLAG_READ が設定されていない場合は、それを設定し、保留中の読み取りのレポートをキャンセルします。
    
CLEAR_READ_FLAG フラグを設定すると各メッセージの**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_READ フラグをオフに、読み取りのレポートを送信しません。 
  
GENERATE_RECEIPT_ONLY フラグが設定されている場合は、すべての保留中の読み取りレポートを送信します。 MSGFLAG_READ を設定したりクリアの操作を行います。
  
SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されているときにプロパティを設定、PR_READ_RECEIPT_REQUESTED FALSE に設定されている場合、読み取りのレポートを送信しません。
  
特定の条件下でのリードのレポートの生成を抑制することによって、レポートの動作を最適化できます。 ただし、レポートの抑制をサポートしていないクライアントは、SUPPRESS_RECEIPT フラグを設定して**SetReadFlag**を呼び出す場合は、MAPI_E_NO_SUPPRESS を取得します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI では、 **IMessage::SetReadFlag**メソッドを使用して、選択したメッセージに開封のフラグを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

