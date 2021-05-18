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
  
> [out]メッセージの返されるインターフェイスへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
S_FALSE 
  
> 呼び出し元のフォームにメッセージが現在存在しません。
    
## <a name="remarks"></a>注釈

フォームは **IMAPIMessageSite::GetMessage** メソッドを呼び出して、現在のメッセージのメッセージ インターフェイスを取得します。 現在のメッセージは [、IPersistMessage::InitNew](ipersistmessage-initnew.md) [、IPersistMessage::Load、](ipersistmessage-load.md)または [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) メソッドで以前に渡されたメッセージと同じです。 
  
 **GetMessage は** 、現在S_FALSEメッセージが存在しない場合、そのメッセージを返します。 この状態は [、IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出した後、または **IPersistMessage::Load または IPersistMessage::SaveCompleted** の次の呼び出しが行われる前に発生する可能性があります。  
  
フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI は **IMAPIMessageSite::GetMessage** メソッドを使用して、現在キャッシュされているメッセージ ポインター (使用可能な場合) を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

