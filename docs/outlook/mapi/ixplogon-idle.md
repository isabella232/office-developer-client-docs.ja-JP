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
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578014"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

