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
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575869"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
個人用フォルダー (.pst) ファイルの登録の一覧を取得します。
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>パラメーター

 _ppmval_
  
> [in][SPropValue](spropvalue.md)構造体へのポインターへのポインター。 この構造体の ulPropTag メンバーは、型の PT_MV_UNICODE と MVszW の値のメンバーが null で終わる Unicode 文字列の配列になります。 これらの文字列は、登録の永続化するための Dll へのパスです。 
    
> [!NOTE]
> ANSI .pst のサポートが実装されていません。 
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 関数の呼び出しに成功しました。
    
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

