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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bb373e4b666f44c432ac1b04c0449eb7f0408a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592935"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
新規または既存のメッセージがフォームで読み込まれているフォーム ビューアーを通知します。
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)または[IPersistMessage::Load](ipersistmessage-load.md)のいずれかのメソッドを使用してフォームのメッセージが読み込まれるたびに、 **IMAPIViewAdviseSink::OnNewMessage**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

ビューアーが以前に表示するメッセージを示していないために、フォーム オブジェクトをアクティブにマウス ポインターを解放します。 
  
フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

