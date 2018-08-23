---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f49ea23ed7fef91bcb360483611af2ee60429934
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592970"
---
# <a name="imapiviewadvisesinkonshutdown"></a>IMAPIViewAdviseSink::OnShutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム ビューアーに、フォームが閉じられることを通知します。
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

