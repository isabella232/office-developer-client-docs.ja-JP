---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: 予定を予定表フォルダーを再配置をサポートします。
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799492"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

予定を予定表フォルダーを再配置をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |**IUnknown** <br/> |
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|によって実装されます。  <br/> |tzmovelib.dll  <br/> |
|によって呼び出されます。  <br/> |MAPI クライアント アプリケーション  <br/> |
|公開されます。  <br/> |Outlook の再配置オブジェクト  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |予定は予定、 **EndEnumerateAppointments**から取得した通常のリストを再配置するためのタスクを開始します。  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |完了する再配置を予定するまで待機し、結果を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

