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
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800367"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**適用されます**: Outlook 
  
アクティブなセッションへの接続をキャンセルします。
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [In]予約されています。0 へのポインターである必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 接続は取り消されました。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

**Shutdown**メソッドの実装では、どのようなタスクを検討する必要を実行します。 MAPI は、すべてのログオン オブジェクトをリリースした後にのみ、 **Shutdown**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IABProvider: IUnknown](iabprovideriunknown.md)

