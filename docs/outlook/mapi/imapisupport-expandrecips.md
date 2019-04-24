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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316528"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の配布リストを展開し、メッセージの受信者の一覧を完成させる。
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpmessage_
  
> 順番処理する受信者リストがあるメッセージへのポインター。
    
 _lアウトフラグ_
  
> 読み上げ発生する処理の種類を制御するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
NEEDS_PREPROCESSING 
  
> メッセージを送信する前に前処理する必要があります。
    
NEEDS_SPOOLER 
  
> MAPI スプーラー (発信者が密接に結合されているトランスポートプロバイダーではない) は、メッセージを送信する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージの宛先リストが正常に処理されました。
    
## <a name="remarks"></a>解説

**imapisupport:: ExpandRecips**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは**ExpandRecips**を呼び出して、次のタスクを実行するように MAPI に通知します。 
  
- 特定の個人用配布リストをコンポーネントの受信者に展開します。
    
- 変更されたすべての表示名を元の名前に置き換えます。
    
- 重複しているエントリをマークします。
    
- 1回限りのすべての住所を解決します。 
    
- メッセージにプリプロセスが必要かどうかを確認し、実行されている場合は、 _lNEEDS_PREPROCESSING フラグ_が指すフラグをに設定します。 
    
 **ExpandRecips**は、メッセージアドレスの種類が mapipdl であるすべての配布リストを展開します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ処理の一部として**ExpandRecips**を常に呼び出します。 [IMessage:: submitmessage](imessage-submitmessage.md)メソッド実装の最初の呼び出しの1つを**ExpandRecips**に呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

