---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: de450ddef3990f788f3e92ac39b15345aa3adf62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630566"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージまたは既存のメッセージがフォームに読み込まれたとフォーム ビューアーに通知します。
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは [、IPersistMessage::InitNew](ipersistmessage-initnew.md)メソッドまたは [IPersistMessage::Load](ipersistmessage-load.md)メソッドを使用してフォームにメッセージが読み込まれるたびに **IMAPIViewAdviseSink::OnNewMessage** メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

アクティブなポインターをフォーム オブジェクトに離すのは、ビューアーが以前表示したメッセージを指し示しなくなったためです。 
  
フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

