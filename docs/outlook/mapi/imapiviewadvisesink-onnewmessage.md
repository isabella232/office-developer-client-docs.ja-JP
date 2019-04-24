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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328792"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームビューアーに、新規または既存のメッセージがフォームにロードされたことを通知します。
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知に成功しました。
    
## <a name="remarks"></a>解説

form オブジェクトは、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)または[IPersistMessage:: Load](ipersistmessage-load.md)メソッドのいずれかを使用して、フォームにメッセージが読み込まれるたびに**IMAPIViewAdviseSink:: onnewmessage**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

閲覧者が以前に表示していたメッセージをポイントしていないため、アクティブポインターをフォームオブジェクトに解放します。 
  
フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

