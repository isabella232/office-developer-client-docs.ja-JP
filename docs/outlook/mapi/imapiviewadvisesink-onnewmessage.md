---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419605"
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

