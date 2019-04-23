---
title: ログ ファイルの使用領域の最小化
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288877"
---
# <a name="minimizing-log-file-space-usage"></a>ログ ファイルの使用領域の最小化

**適用先:** Access 2013、Office 2013

A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.

**Microsoft SQL Server 6.5 でチェックポイント時のログの切り捨てを有効にするには**

1.  Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。

2.  この機能を有効にするデータベースの名前をダブルクリックします。

3.  From the **Database** tab, select **Truncate**.

4.  From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.

**Microsoft SQL Server 7.0 でチェックポイント時のログの切り捨てを有効にするには**

1.  Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベースのツリーを開きます。

2.  Right-click the name of the database on which this feature will be enabled and choose **Properties**.

3.  From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.

For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.

