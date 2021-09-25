---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 54e587ef23c9b121d4b9dc57bd68ebdad5ec38f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584200"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーを順番に閉じます。
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは、トランスポート プロバイダーのシャットダウンに成功しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、トランスポート プロバイダー オブジェクトを解放する前に **IXPProvider::Shutdown** メソッドを呼び出します。 Shutdown を **呼び出す** 前に、MAPI はプロバイダーのすべてのログオン オブジェクトを解放します。
  
## <a name="see-also"></a>関連項目



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

