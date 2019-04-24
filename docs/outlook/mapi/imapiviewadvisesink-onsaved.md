---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351199"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの現在のメッセージが保存されたことをフォームビューアーに通知します。
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

form オブジェクトは、フォーム内の現在のメッセージが正常に保存された後に、 **IMAPIViewAdviseSink:: onsaved**メソッドを呼び出します。 これにより、閲覧者は、メッセージの変更を反映するように windows を更新することができます。 
  
フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

