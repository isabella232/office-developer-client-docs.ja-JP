---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: 予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。
ms.openlocfilehash: 9472f9b1da9db435b8deba12c4468c02311098ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605373"
---
# <a name="iolkapptrebaserendenumerateappointments"></a>IOlkApptRebaser::EndEnumerateAppointments

予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a>パラメーター

_pContext_
  
> [in]必要があります。[IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)の前回の呼び出しから取得されたコンテキストへのポインター。
    
_phResult_
  
> [out]必要があります。列挙操作の結果を取得するためには、 **HRESULT** へのポインター。 
    
_ppError_
  
> [out]省略可能です。拡張エラー情報を取得する **MAPIERROR** 構造体へのポインターへのポインター。 
    
_ppRows_
  
> [out]必要があります。再配置する必要がある予定を記述する[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)構造体へのポインターへのポインター。通常、この構造体は[IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)に渡されます。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

