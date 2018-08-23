---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d5d86af111bc778839a78f9b56ba7126e6c973d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567378"
---
# <a name="imapimessagesitegetsession"></a>IMAPIMessageSite::GetSession

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在のメッセージを作成または開いたの MAPI セッションを返します。
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a>パラメーター

 _ppSession_
  
> [out]返されたセッション オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
S_FALSE 
  
> 現在のメッセージのセッションが存在しません。
    
## <a name="remarks"></a>注釈

フォームのサーバーに関連付けられているインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI メソッドを使用して、 **IMAPIMessageSite::GetSession**現在キャッシュされているセッションのポインターを返すことがある場合。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

