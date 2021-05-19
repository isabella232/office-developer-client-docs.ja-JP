---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: 予定表フォルダー内の予定の再バーズをサポートします。
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410071"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

予定表フォルダー内の予定の再バーズをサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |**IUnknown** <br/> |
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|実装元:  <br/> |tzmovelib.dll  <br/> |
|呼び出し元:  <br/> |MAPI クライアント アプリケーション  <br/> |
|次の場合に公開されます。  <br/> |Outlookの再バーズ  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |通常 **EndEnumerateAppointments** から取得される予定の一覧を指定して、予定の再予約のタスクを開始します。  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |完了する再配置を予定するまで待機し、結果を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

