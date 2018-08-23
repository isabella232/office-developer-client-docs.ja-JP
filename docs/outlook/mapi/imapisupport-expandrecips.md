---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591011"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの受信者リスト、特定の配布リストの展開を完了します。
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]処理する受信者のリストがあるメッセージへのポインター。
    
 _lpulFlags_
  
> [out]発生する処理の種類を制御するフラグのビットマスクへのポインター。 次のフラグを設定することができます。
    
NEEDS_PREPROCESSING 
  
> メッセージが送信される前に前処理が必要に必要です。
    
NEEDS_SPOOLER 
  
> MAPI スプーラーではなく、トランスポート プロバイダーは、呼び出し元が密に結合されている) は、メッセージを送信する必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージの受信者の一覧が正常に処理されました。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::ExpandRecips**メソッドを実装します。 メッセージ ストア プロバイダーは、次のタスクを実行するための MAPI メッセージを表示するのには**ExpandRecips**を呼び出します。 
  
- そのコンポーネントの受信者に、特定の個人用配布リストを展開します。
    
- 変更されたすべての表示名を元の名前に置き換えます。
    
- 重複するエントリをマークします。
    
- 1 回限りのすべてのアドレスを解決します。 
    
- かどうか、メッセージの前処理を必要し場合は、NEEDS_PREPROCESSING に_lpulFlags_で指定されたフラグを設定を確認してください。 
    
 **ExpandRecips**は、MAPIPDL のメッセージのアドレスの種類を持つすべての配布リストを展開します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

常に、メッセージの処理の一部として**ExpandRecips**を呼び出します。 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの実装では、 **ExpandRecips** 1 つの最初の呼び出しへの呼び出しを確認します。 
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

