---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: 予定を再配置する通常IOlkApptRebaser::EndEnumerateAppointmentsから取得予定の一覧を指定するためのタスクを開始します。
ms.openlocfilehash: 2becb305eebe448e2adecf91c2a111f86d97fe50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799504"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a>IOlkApptRebaser::BeginRebaseAppointments

予定を再配置する通常[IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)から取得予定の一覧を指定するためのタスクを開始します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkApptRebaser](iolkapptrebaser.md) を参照してください。
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a>パラメーター

_pRows_
  
> [in]必要があります。再配置する必要がある予定を記述する[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)構造体へのポインター。通常、この構造体は[IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)の前回の呼び出しから取得されます。
    
_pfnProgress_
  
> [in]省略可能です。進行状況が表示されることを再作業の進行状況関数へのポインター。 **PFNREBASETASKPROGRESS** は、tzmovelib.h で定義されます。 
    
_pfnComplete_
  
> [out]省略可能です。再配置の完了の通知を受信するには、再作業完了関数へのポインター。 **PFNREBASETASKCOMPLETE** は、tzmovelib.h で定義されます。 
    
_ppContext_
  
> [out]必要があります。返されるコンテキストへのポインターへのポインター。このコンテキストは、通常[IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)に渡されます。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

このタスクは、新しいスレッドで実行されます。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

