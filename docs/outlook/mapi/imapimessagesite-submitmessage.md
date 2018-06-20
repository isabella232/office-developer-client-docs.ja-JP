---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800606"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**適用されます**: Outlook 
  
現在のメッセージが配信のキューに置かれることを要求します。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]メッセージの送信方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
FORCE_SUBMIT 
  
> MAPI は、場合でも、すぐに送信されない可能性があります、そのメッセージを送信する必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム オブジェクトは、メッセージが配信のキューに置かれることを要求する**IMAPIMessageSite::SubmitMessage**メソッドを呼び出します。 メッセージのサイトでは、メッセージを送信する前に、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出す必要があります。 メッセージは、メッセージが変更されている場合に保存するメッセージが発生する必要があります**SubmitMessage の**ために既に保存されている必要はありません。 **SubmitMessage**の戻り値は後、フォームは現在のメッセージを確認し、存在しない場合はそれ自体を終了してください。 
  
フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI では、 **IMAPIMessageSite::SubmitMessage**メソッドを使用してメッセージを保存します。 最初に、 **IPersistMessage::HandsOffMessage**メソッドを呼び出すことと、 **SubmitMessage**を呼び出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームのインタ フェース](mapi-form-interfaces.md)

