---
title: imapisupportreadreceipt
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425324"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの読み取りまたは非開封レポートを生成します。
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番読み取りまたは非開封レポートの生成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NON_READ 
  
> 非開封レポートが生成されます。 MAPI_NON_READ が設定されていない場合は、読み取りレポートが生成されます。
    
 _lpReadMessage_
  
> 順番レポートを生成するメッセージへのポインター。
    
 _lppemptymessage_
  
> [入力]入力時に、 _lppemptymessage_は空のメッセージへのポインターを指します。 出力では、 _lppemptymessage_はレポートメッセージへのポインターを指します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> レポートが正常に生成されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: readreceipt**メソッドは、メッセージストアプロバイダーサポートオブジェクトに対してのみ実装されます。 メッセージストアプロバイダーは、 **readreceipt**を呼び出して、MAPI に、 _lpReadMessage_パラメーターによって示されるメッセージの読み取りレポートまたは非開封レポートを生成するように指示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されていて、次のいずれかの条件に該当する場合は、 **readreceipt**を呼び出します。
  
- メッセージが開封されました。
    
- メッセージが移動されました。
    
- メッセージがコピーされました。
    
- メッセージの[IMessage:: setreadflag](imessage-setreadflag.md)メソッドが呼び出されました。 
    
メッセージが削除されたときに、 **readreceipt**を呼び出しません。 
  
読み取りまたは非開封レポートは、メッセージに対して1回だけ送信する必要があります。 メッセージの開封状態を追跡し、1つのメッセージに対して複数のレポートを送信しません。
  
MAPI が**readreceipt**から返されたときに、 _lppemptymessage_パラメーターが有効なレポートメッセージを指している場合は、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出してメッセージを送信し、 **IUnknown: s: release を呼び出してポインターを解放します。** メソッド。 
  
**readreceipt**が失敗した場合、メッセージは送信されずに解放される必要があります。 メッセージの開封状態を格納する場合は、後で読み取りまたは非開封レポートを生成することができます。 
  
フォルダー内のストアによって生成される読み取りおよび非開封レポートを表示または非表示にすることができます。 読み取りおよび非開封レポートを隠しフォルダーに格納することで、より厳密なセキュリティを実装できます。
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[PidTagReadReceiptRequested 標準プロパティ](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

