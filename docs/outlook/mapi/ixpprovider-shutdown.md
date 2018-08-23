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
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801264"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**適用対象**: Outlook 
  
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

