---
title: トランザクションを制御する
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ced1ae7b32d25fbae53c670959a4a6c77bcea0be
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716623"
---
# <a name="controlling-transactions"></a>トランザクションを制御する


**適用されます**Access 2013、Office 2013。

*トランザクション*では、先頭と末尾の一連の接続の両端でデータ アクセス操作を区切ります。 トランザクションの機能によって、データ ソース、**接続**オブジェクトも使用するを作成し、トランザクションを管理できます。 たとえば、Microsoft SQL Server 2000 上のデータベースにアクセスするには、Microsoft OLE DB プロバイダーの SQL Server を使用して、作成できますを実行するコマンドの複数の入れ子になったトランザクション。

ADO では、トランザクション内の操作によって発生するデータ ソースの変更が、すべて正常に実行されるか、まったく実行されないかのいずれかになります。

トランザクションが取り消されるか、その操作のうちいずれかが失敗した場合、最終的には、トランザクション内の操作がまったく発生しなかったときと同じ結果になります。データ ソースは、トランザクションの開始前と同じ状態のままです。

ADO のオブジェクト モデルでは、トランザクションは明示的に定義されていませんが、**Connection** オブジェクトの一連のメソッド (**BeginTrans**、**CommitTrans**、および **RollbackTrans**) として表現されています。

トランザクションの詳細については、「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

