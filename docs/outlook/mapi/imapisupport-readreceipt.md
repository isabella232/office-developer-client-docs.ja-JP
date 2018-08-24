---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e785d42639d51dab154a0bde239f858a92ddd143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588623"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
読み取りまたはメッセージの nonread のレポートを生成します。
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]読み取りまたは nonread のレポートの生成方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_NON_READ 
  
> Nonread のレポートが生成されます。 MAPI_NON_READ が設定されていない場合は、リードのレポートが生成されます。
    
 _lpReadMessage_
  
> [in]レポートを生成するかについては、メッセージへのポインター。
    
 _lppEmptyMessage_
  
> [で [チェック アウト]入力では、 _lppEmptyMessage_は、空のメッセージへのポインターを指しています。 出力では、 _lppEmptyMessage_は、レポート メッセージへのポインターをポイントします。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> レポートが正常に生成されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::ReadReceipt**メソッドは、メッセージ ストア プロバイダーのサポートのオブジェクトに対してのみ実装されます。 メッセージ ストア プロバイダーは、読み取りまたは_lpReadMessage_パラメーターで指定されたメッセージの nonread のレポートを生成するための MAPI に指示するために**ReadReceipt**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されて、次の条件のいずれかが true の場合は、 **ReadReceipt**を呼び出します。
  
- メッセージが読み取られています。
    
- メッセージを移動するとします。
    
- メッセージがコピーされました。
    
- メッセージの[IMessage::SetReadFlag](imessage-setreadflag.md)メソッドが呼び出されました。 
    
メッセージが削除されると、 **ReadReceipt**を呼び出さないようにします。 
  
読み取りまたは nonread のレポートは、メッセージの 1 回だけ送信してください。 メッセージの読み取り状態を追跡し、1 つのメッセージの複数のレポートを送信できません。
  
_LppEmptyMessage_パラメーターは、MAPI は、 **ReadReceipt**から返されるときに、有効なレポートのメッセージをポイントしている場合、メッセージを送信し、その**の IUnknown:s:Release を呼び出すことによって、ポインターを解放する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出す**メソッドです。 
  
**ReadReceipt**が失敗した場合、送信されることがなくメッセージを解放する必要があります。 メッセージの読み取り状態を保存する場合は後で、読み取りまたは nonread のレポートを生成しようとすることができます。 
  
非表示にするか、フォルダー内のストアによって生成される読み取りおよび nonread のレポートを表示します。 隠しフォルダーに読み取りおよび nonread のレポートを格納する、強固なセキュリティを実装できます。
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[PidTagReadReceiptRequested 標準プロパティ](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

