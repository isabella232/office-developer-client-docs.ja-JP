---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d7a3b61760b21ee34d5726e9a321fd418c55d7ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613752"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システムがアイドル状態で、トランスポート プロバイダーが優先度の低い操作を実行できる状態を示します。
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、呼び出しの XP_LOGON_SP フラグを現在のセッションを開いた [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドに渡して、システムがアイドル状態にあるときに、要求された場合に定期的に **IXPLogon::Idle** メソッドを呼び出します。 システムがアイドル状態の場合、トランスポート プロバイダーは、他の呼び出し中に適切ではない、または定期的に発生する必要があるバックグラウンド操作を実行できます。 
  
## <a name="see-also"></a>関連項目



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

