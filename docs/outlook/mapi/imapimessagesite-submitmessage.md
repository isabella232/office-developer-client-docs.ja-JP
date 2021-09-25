---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fce66a5c7a306df2d116f473458e7155739eb750
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630699"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージを配信キューに入れろという要求。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]メッセージの送信方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
FORCE_SUBMIT 
  
> MAPI は、すぐに送信されない可能性がある場合でも、メッセージを送信する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIMessageSite::SubmitMessage** メソッドを呼び出して、メッセージの配信キューに入れられます。 メッセージ サイトは、メッセージを送信する前に [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) メソッドを呼び出す必要があります。 メッセージが変更された場合 **、SubmitMessage** によってメッセージが保存される必要があるため、メッセージを以前に保存する必要はなされません。 SubmitMessage が返 **された後**、フォームは現在のメッセージをチェックし、存在しない場合は自分自身を閉じなければならない。 
  
フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI は **IMAPIMessageSite::SubmitMessage** メソッドを使用してメッセージを保存します。 まず **、IPersistMessage::HandsOffMessage** メソッドを呼び出し、次に **SubmitMessage を呼び出します**。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

