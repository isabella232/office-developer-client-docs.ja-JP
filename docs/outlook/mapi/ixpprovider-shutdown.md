---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592606"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
適切な順序でトランスポート プロバイダーを閉じます。
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> トランスポート プロバイダーのシャット ダウンの呼び出しに成功しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーでは、トランスポート プロバイダーのオブジェクトを解放する前に**IXPProvider::Shutdown**メソッドを呼び出します。 **シャット ダウン**を呼び出す前に、MAPI は、プロバイダーのすべてのログオン オブジェクトを解放します。
  
## <a name="see-also"></a>関連項目



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

