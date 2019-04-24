---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: 予定表フォルダー内の予定の再配置をサポートします。
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321862"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

予定表フォルダー内の予定の再配置をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |**IUnknown** <br/> |
|ヘッダー ファイル:  <br/> |、tzmovelib.h  <br/> |
|実装元:  <br/> |、tzmovelib.h  <br/> |
|呼び出し元:  <br/> |MAPI クライアントアプリケーション  <br/> |
|公開:  <br/> |Outlook のリベース/再配置オブジェクト  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。  <br/> |
|**[beginrebaseappointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |通常**EndEnumerateAppointments**から取得された予定の一覧がある場合、予定の再配置のタスクを開始します。  <br/> |
|**[endrebaseappointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |完了する再配置を予定するまで待機し、結果を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

