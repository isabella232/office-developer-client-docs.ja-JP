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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321407"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージが配信のためにキューに入れられるように要求します。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番メッセージの送信方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
FORCE_SUBMIT 
  
> MAPI は、メッセージがすぐに送信されない可能性がある場合でも、メッセージを送信する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

Form オブジェクトは**IMAPIMessageSite:: submitmessage**メソッドを呼び出して、メッセージが配信のためにキューに入れられるよう要求します。 メッセージサイトは、メッセージを送信する前に、 [IPersistMessage::](ipersistmessage-handsoffmessage.md)配布用のメッセージメソッドを呼び出す必要があります。 メッセージが変更された場合、 **submitmessage**によってメッセージが保存されるため、メッセージを以前に保存しておく必要はありません。 **submitmessage**を戻すと、フォームは現在のメッセージを確認し、存在しない場合は自分自身を破棄する必要があります。 
  
フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: submitmessage  <br/> |mfcmapi は、 **IMAPIMessageSite:: submitmessage**メソッドを使用して、メッセージを保存します。 最初に、 **IPersistMessage:: handsoffmessage**メソッドを呼び出して、 **submitmessage**を呼び出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームインターフェイス](mapi-form-interfaces.md)

