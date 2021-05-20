---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436049"
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

