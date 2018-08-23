---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579446"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム ビューアーの現在のメッセージが MAPI スプーラーに送信されたことを通知します。
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、 [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)への呼び出しが正常に返された後に、 **IMAPIViewAdviseSink::OnSubmitted**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**OnSubmitted**が呼び出されると、メッセージが更新されたことを前提として続行できます。 発生した変更を反映するように、windows を更新します。 
  
フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

