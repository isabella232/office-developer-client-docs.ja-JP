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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801253"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**適用対象**: Outlook 
  
システムがアイドル状態、優先度の低い操作を実行するトランスポート プロバイダーを有効にすることを示します。
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、時間の場合、システムがアイドル状態、現在のセッションを開いている[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドの呼び出しで、XP_LOGON_SP フラグを渡すことによって、要求された場合定期的に、 **IXPLogon::Idle**メソッドを呼び出します。 システムがアイドル状態のときに、トランスポート プロバイダーは、適切な他の呼び出し時にまたは定期的に発生する必要があるバック グラウンドの操作を実行できます。 
  
## <a name="see-also"></a>関連項目



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

