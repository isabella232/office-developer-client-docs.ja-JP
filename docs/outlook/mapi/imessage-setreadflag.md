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
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349267"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> 順番メッセージの読み取りフラグの設定を制御するフラグのビットマスクです。このフラグは、メッセージの MSGFLAG_READ フラグが**PR_MESSAGE_FLAGS**プロパティで、開封レポートの処理になります。 次のフラグを設定できます。 
    
  - CLEAR_READ_FLAG: MSGFLAG_READ フラグは**PR_MESSAGE_FLAGS**でクリアされ、閲覧レポートは送信されません。 
      
  - CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDING フラグは**PR_MESSAGE_FLAGS**ではクリアされ、非開封レポートは送信されないようにする必要があります。 
      
  - CLEAR_RN_PENDING: MSGFLAG_RN_PENDING フラグは**PR_MESSAGE_FLAGS**でクリアされ、閲覧レポートは送信されません。 
      
  - GENERATE_RECEIPT_ONLY: 読み取りレポートは、保留中の場合は送信されますが、MSGFLAG_READ フラグの状態は変更されません。
      
  - MAPI_DEFERRED_ERRORS: **setreadflag**が正常に返されるようにします。操作が完了する前である可能性があります。 
      
  - SUPPRESS_RECEIPT: 読み取りレポートが要求されている場合は、保留中の読み取りレポートを取り消す必要があります。この呼び出しは、メッセージの状態を未読から読み取りに変更します。 この呼び出しでメッセージの状態が変更されない場合、メッセージストアプロバイダーはこのフラグを無視できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの read フラグが正常に設定またはクリアされました。
    
MAPI_E_NO_SUPPRESS 
  
> メッセージストアプロバイダーは、閲覧レポートの抑制をサポートしていません。
    
MAPI_E_INVALID_PARAMETER 
  
> 次のフラグの組み合わせのいずれかが_ulflags_パラメーターで設定されています。 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>解説

**IMessage:: setreadflag**メソッドは、 **PR_MESSAGE_FLAGS**プロパティのメッセージの MSGFLAG_READ フラグを設定またはクリアし、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出してメッセージを保存します。 MSGFLAG_READ フラグを設定すると、メッセージは開封済みとしてマークされます。これは、意図した受信者が実際にメッセージを読んでいることを示すわけではありません。 
  
**setreadflags**は、閲覧レポートの送信も管理します。 閲覧レポートが送信されるのは、送信者が1人を要求した場合のみです。 
  
読み取りフラグは次のように変更できません。
  
- 存在しないメッセージ。
    
- 他の場所に移動されたメッセージ。
    
- 読み取り/書き込みアクセス許可で開いているメッセージ。
    
- 現在送信されているメッセージ。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

_ulflags_パラメーターにどのフラグも設定されていない場合は、次のルールが適用されます。 
  
- MSGFLAG_READ が既に設定されている場合は、何も実行しません。
    
- MSGFLAG_READ が設定されていない場合は、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は設定し、保留中の読み取りレポートを送信します。
    
SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合は、PR_READ_RECEIPT_REQUESTED ビット (設定されている場合) をクリアし、閲覧レポートを送信しないようにする必要があります。
  
SUPPRESS_RECEIPT フラグが設定されている場合:
  
- MSGFLAG_READ が既に設定されている場合は、何も実行しません。 
    
- MSGFLAG_READ が設定されていない場合は、設定し、保留中のすべての開封レポートを取り消します。
    
CLEAR_READ_FLAG フラグが設定されている場合は、各メッセージの**PR_MESSAGE_FLAGS**プロパティの MSGFLAG_READ フラグをオフにして、読み取りレポートを送信しないようにします。 
  
GENERATE_RECEIPT_ONLY フラグが設定されている場合は、保留中のすべての読み取りレポートを送信します。 MSGFLAG_READ を設定またはクリアしません。
  
SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合は、PR_READ_RECEIPT_REQUESTED プロパティが設定されている場合は FALSE に設定し、閲覧レポートを送信しないようにします。
  
特定の条件下での読み取りレポートの生成を抑制することで、レポートの動作を最適化できます。 ただし、レポートの抑制をサポートしておらず、クライアントが SUPPRESS_RECEIPT フラグを設定して**setreadflag**を呼び出している場合は、MAPI_E_NO_SUPPRESS を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |cfolderdlg:: OnSetReadFlag  <br/> |mfcmapi は、 **IMessage:: setreadflag**メソッドを使用して、選択されたメッセージに対する読み取りフラグを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

