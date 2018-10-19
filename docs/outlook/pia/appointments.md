---
title: 予定
TOCTitle: Appointments
ms:assetid: 989a94a8-c1dc-4c5d-ab2b-2cc29a08f8a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184627(v=office.15)
ms:contentKeyID: 55119805
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 79685e89457256ca213d9e1d0ce474e25b755e39
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406261"
---
# <a name="appointments"></a>予定

このセクションでは、予定に関連するサンプル タスクを示します。予定には、イベント、会議、定期的な予定などがあります。Outlook の予定表フォルダー内の予定は、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトで表されます。

## <a name="in-this-section"></a>このセクションの内容

|トピック|説明|
|:----|:----------|
|[終日イベントの予定を作成する](how-to-create-an-appointment-that-is-an-all-day-event.md)  |[AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) プロパティを使用して、終日イベントである予定を作成します。|
|[太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)  |太平洋タイム ゾーン (UTC-8) で開始して東部タイム ゾーン (UTC-5) で終了する予定を作成します。|
|[予定アイテムに異なる受信者の種類を指定する](how-to-specify-different-recipient-types-for-an-appointment-item.md)  |[OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) 列挙型を使用して、予定アイテムにさまざまな受信者の種類を指定します。|
|[既定の定期的なパターンを使用して、定期的な予定を作成する](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)  |既定の定期的なパターンを使用して、定期的な予定を作成します。|
|[週単位パターンの定期的な予定を作成する](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)  |週単位パターンの定期的な予定 (毎週月曜日、水曜日、および金曜日に行う予定など) を作成します。|
|[YearNth パターンの年単位の定期的な予定を作成する](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)  |6 月の第 1 月曜日など、毎年 1 回の特定の曜日を指定した定期的な予定を作成します。|
|[定期的な一連の予定から特定の予定を検索する](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)  |一連の定期的な予定のうちの特定の予定を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを取得する方法を示します。|
|[定期的な一連の予定に例外的な予定を作成する](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)  |[Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトを使用して、予定に対する標準の定期的なパターンの例外を作成します。|
|[予定アイテムのリマインダーを作成する](how-to-create-a-reminder-for-an-appointment-item.md)  |[ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) プロパティを使用して、予定アイテムの事前通知を作成します。|
|[予定の XML データを Outlook の予定オブジェクトにインポートする](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)  |XML 形式の予定データを読み込み、そのデータを Outlook の既定の予定表内の AppointmentItem オブジェクトに保存し、予定オブジェクトを配列として返します。|

## <a name="see-also"></a>関連項目

- [予定表](calendar.md)
- [会議出席依頼](meeting-requests.md)
- [操作方法 (Outlook 2013 PIA リファレンス)](how-do-i-outlook-2013-pia-reference.md)

