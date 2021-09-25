---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 67dac1246a2d01557ce2d6167f5f3eb32cb57a38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592292"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージが MAPI スプーラーに送信されたとフォーム ビューアーに通知します。
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは [、IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)の呼び出しが正常に返された後 **、IMAPIViewAdviseSink::OnSubmitted** メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**OnSubmitted が** 呼び出された後、メッセージが更新されたという前提で続行できます。 発生した変更を反映するようにウィンドウを更新します。 
  
フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

