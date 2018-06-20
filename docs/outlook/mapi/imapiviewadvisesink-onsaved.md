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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800872"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**適用されます**: Outlook 
  
フォームの現在のメッセージが保存されているフォーム ビューアーを通知します。
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Parameters

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム オブジェクトは、フォームの現在のメッセージが正常に保存された後に、 **IMAPIViewAdviseSink::OnSaved**メソッドを呼び出します。 これを行うメッセージへの変更を反映するように、windows を更新するためのビューアーを使用できます。 
  
フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)

