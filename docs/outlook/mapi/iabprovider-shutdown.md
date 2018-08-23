---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567889"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アクティブなセッションへの接続をキャンセルします。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [In]予約されています。0 へのポインターである必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 接続は取り消されました。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

**Shutdown**メソッドの実装では、どのようなタスクを検討する必要を実行します。 MAPI は、すべてのログオン オブジェクトをリリースした後にのみ、 **Shutdown**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IABProvider : IUnknown](iabprovideriunknown.md)

