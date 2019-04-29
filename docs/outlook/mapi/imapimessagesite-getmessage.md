---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409028"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージを返します。
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>パラメーター

 _ppmsg_
  
> 読み上げメッセージに対して返されるインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
S_FALSE 
  
> 呼び出し元フォームのメッセージは現在存在しません。
    
## <a name="remarks"></a>注釈

フォームは、 **IMAPIMessageSite:: GetMessage**メソッドを呼び出して、現在のメッセージのメッセージインターフェイスを取得します。 現在のメッセージは、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)、 [IPersistMessage:: Load](ipersistmessage-load.md)、または[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)メソッドで以前に渡されたのと同じメッセージです。 
  
 現在、メッセージが存在しない場合、 **GetMessage**は S_FALSE を返します。 この状態は、 [IPersistMessage:: handsoffmessage](ipersistmessage-handsoffmessage.md)メソッドへの呼び出し、または**IPersistMessage:: Load**または**IPersistMessage:: SaveCompleted**の次の呼び出しの前に発生する可能性があります。 
  
フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: getsession  <br/> |mfcmapi は、 **IMAPIMessageSite:: GetMessage**メソッドを使用して、現在キャッシュされているメッセージポインター (使用可能な場合) を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームインターフェイス](mapi-form-interfaces.md)

