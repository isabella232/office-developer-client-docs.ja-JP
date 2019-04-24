---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321946"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a>IOlkApptRebaser::BeginEnumerateAppointments

タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a>パラメーター

_pfnprogress_
  
> [in]省略可能です。進行状況が表示されることを再作業の進行状況関数へのポインター。 **PFNREBASETASKPROGRESS** は、tzmovelib.h で定義されます。 
    
_ppcontext_
  
> [out]必要があります。返されるコンテキストへのポインターへのポインター。このコンテキストは、 [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)に渡されます。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

このタスクは、新しいスレッドで実行されます。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

