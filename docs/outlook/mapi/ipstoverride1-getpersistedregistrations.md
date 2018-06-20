---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801163"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**適用されます**: Outlook 
  
個人用フォルダー (.pst) ファイルの登録の一覧を取得します。
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameters

 _ppmval_
  
> [in][SPropValue](spropvalue.md)構造体へのポインターへのポインター。 この構造体の ulPropTag メンバーは、型の PT_MV_UNICODE と MVszW の値のメンバーが null で終わる Unicode 文字列の配列になります。 これらの文字列は、登録の永続化するための Dll へのパスです。 
    
> [!NOTE]
> ANSI .pst のサポートが実装されていません。 
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 関数の呼び出しに成功しました。
    
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1: IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ: IUnknown](ipstoverridereqiunknown.md)

