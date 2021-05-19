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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415132"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダー (.pst) ファイルの登録の一覧を取得します。
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>パラメーター

 _ppmval_
  
> [in] [SPropValue](spropvalue.md) 構造体へのポインターを指すポインター。 この構造体の ulPropTag メンバーは PT_MV_UNICODE 型であり、MVszW 値メンバーは null 終端 Unicode 文字列の配列になります。 これらの文字列は、登録が保持されている DLL へのパスです。 
    
> [!NOTE]
> ANSI の .pst サポートは実装されていません。 
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 関数呼び出しが成功しました。
    
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

