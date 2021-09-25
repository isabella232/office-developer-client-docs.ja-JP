---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: de652bef3325ca926e7827c15705dc2411b92fc7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556526"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの受信者リストを完了し、特定の配布リストを展開します。
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]処理する受信者リストを持つメッセージへのポインター。
    
 _lpulFlags_
  
> [out]発生する処理の種類を制御するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
NEEDS_PREPROCESSING 
  
> メッセージを送信する前に、メッセージを前処理する必要があります。
    
NEEDS_SPOOLER 
  
> MAPI スプーラー (呼び出し元が緊密に結合されているトランスポート プロバイダーではなく) は、メッセージを送信する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの受信者リストが正常に処理されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::ExpandRecips** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは **ExpandRecips を呼び出して** 、MAPI に次のタスクを実行するように求めるプロンプトを表示します。 
  
- 特定の個人用配布リストをコンポーネントの受信者に展開します。
    
- 変更された表示名を元の名前に置き換える。
    
- 重複するエントリをマークします。
    
- すべての一時アドレスを解決します。 
    
- メッセージに前処理が必要かどうかを確認し、メッセージが処理する場合は  _、lpulFlags_ が示すフラグを NEEDS_PREPROCESSING。 
    
 **ExpandRecips は** 、MAPIPDL のメッセージング アドレスの種類を持つ配布リストを展開します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ処理の **一部として ExpandRecips** を常に呼び出します。 **ExpandRecips への呼び出しは**[、IMessage::SubmitMessage](imessage-submitmessage.md)メソッド実装の最初の呼び出しの 1 つを行います。 
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

