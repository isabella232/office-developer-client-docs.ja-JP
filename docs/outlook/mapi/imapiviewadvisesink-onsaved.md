---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6b9fbb2eae00357fdc99965b2668f74246d44dd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620815"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの現在のメッセージが保存されたとフォーム ビューアーに通知します。
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、フォーム内の現在のメッセージが正常に保存された後 **、IMAPIViewAdviseSink::OnSaved** メソッドを呼び出します。 これにより、閲覧者はメッセージの変更を反映するようにウィンドウを更新できます。 
  
フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

