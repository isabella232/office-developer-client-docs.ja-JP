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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315471"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダー (.pst) ファイルの登録リストを取得します。
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>パラメーター

 _ppmval_
  
> 順番[spropvalue](spropvalue.md)構造体へのポインターへのポインター。 この構造体の ulPropTag メンバーの型は PT_MV_UNICODE で、MVszW value メンバーは、null で終了する UNICODE 文字列の配列になります。 これらの文字列は、登録が永続化されている dll へのパスです。 
    
> [!NOTE]
> ANSI の .pst サポートは実装されていません。 
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 関数呼び出しが成功しました。
    
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

