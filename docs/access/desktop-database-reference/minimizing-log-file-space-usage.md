---
title: ログ ファイルの使用領域の最小化
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c8d582d55596b7d19220580bc2e670e92bfeb0ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602207"
---
# <a name="minimizing-log-file-space-usage"></a>ログ ファイルの使用領域の最小化

**適用先**: Access 2013、Office 2013

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

