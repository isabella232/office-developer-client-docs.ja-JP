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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295549"
---
# <a name="controlling-transactions"></a>トランザクションを制御する


**適用先:** Access 2013、Office 2013

*トランザクション*は、1つの接続で発生した一連のデータアクセス操作の開始と終了を区切ります。 Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions. For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.

ADO では、トランザクション内の操作によって発生するデータ ソースの変更が、すべて正常に実行されるか、まったく実行されないかのいずれかになります。

トランザクションが取り消されるか、その操作のうちいずれかが失敗した場合、最終的には、トランザクション内の操作がまったく発生しなかったときと同じ結果になります。データ ソースは、トランザクションの開始前と同じ状態のままです。

ADO のオブジェクト モデルでは、トランザクションは明示的に定義されていませんが、**Connection** オブジェクトの一連のメソッド (**BeginTrans**、**CommitTrans**、および **RollbackTrans**) として表現されています。

トランザクションの詳細については、「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

