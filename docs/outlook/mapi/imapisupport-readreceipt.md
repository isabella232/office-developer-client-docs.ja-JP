---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bd008c7233b191c3e187f6cc44767a9b136a2df8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625407"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの読み取りまたは読み取り以外のレポートを生成します。
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]読み取りまたは読み取り以外のレポートの生成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NON_READ 
  
> 読み取り以外のレポートが生成されます。 このMAPI_NON_READ設定されていない場合は、読み取りレポートが生成されます。
    
 _lpReadMessage_
  
> [in]レポートを生成するメッセージへのポインター。
    
 _lppEmptyMessage_
  
> [in, out]入力時に  _、lppEmptyMessage_ は空のメッセージへのポインターを指します。 出力時に  _、lppEmptyMessage_ はレポート メッセージへのポインターを指します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> レポートが正常に生成されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::ReadReceipt** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトにのみ実装されます。 メッセージ ストア プロバイダーは **ReadReceipt** を呼び出して  _、lpReadMessage_ パラメーターが指すメッセージの読み取りまたは読み取り以外のレポートを生成するように MAPI に指示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ReadReceipt** を呼び **出すのは**、PR_READ_RECEIPT_REQUESTED ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定され、次のいずれかの条件が満たされている場合です。
  
- メッセージが読み取らされた。
    
- メッセージが移動されました。
    
- メッセージがコピーされました。
    
- メッセージの [IMessage::SetReadFlag メソッド](imessage-setreadflag.md) が呼び出されました。 
    
メッセージが削除 **された場合は、ReadReceipt** を呼び出さない。 
  
読み取りまたは読み取り以外のレポートは、メッセージに対して 1 回だけ送信する必要があります。 メッセージの読み取り状態を追跡し、1 つのメッセージに対して複数のレポートを送信しない。
  
_LppEmptyMessage_ パラメーターが有効なレポート メッセージを指している場合は、MAPI が **ReadReceipt** から返された場合は [、IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出してメッセージを送信し **、IUnknown:s:Release** メソッドを呼び出してポインターを解放します。 
  
**ReadReceipt が失敗** した場合は、メッセージを送信せずに解放する必要があります。 メッセージの読み取り状態を保存する場合は、後で読み取りまたは読み取り以外のレポートを生成できます。 
  
フォルダー内のストアによって生成された読み取りレポートと読み取り以外のレポートを非表示または表示できます。 読み取りレポートと読み取り以外のレポートを非表示フォルダーに格納すると、セキュリティを強化できます。
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[PidTagReadReceiptRequested 標準プロパティ](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

