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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3612c12a503174484d4a469ffa167922a015ed5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576611"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在のメッセージを返します。
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>パラメーター

 _ppmsg_
  
> [out]メッセージの返されるインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
S_FALSE 
  
> メッセージ現在存在しない呼び出し元のフォームにします。
    
## <a name="remarks"></a>注釈

フォームでは、現在のメッセージのメッセージのインターフェイスを取得する**IMAPIMessageSite::GetMessage**メソッドを呼び出します。 現在のメッセージは、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、 [IPersistMessage::Load](ipersistmessage-load.md)、または[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドに渡されたものでは以前と同じメッセージ。 
  
 メッセージ現在存在しない場合は、**自動インクリメント**は S_FALSE を返します。 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッド、または**IPersistMessage::Load**の次の呼び出しの前に、の呼び出しの後に発生することがこの状態や、 **IPersistMessage::SaveCompleted**が行われます。 
  
フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI メソッドを使用して、 **IMAPIMessageSite::GetMessage** 、現在キャッシュされているメッセージ ポインターを返すことがある場合。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

