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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715278"
---
# <a name="minimizing-log-file-space-usage"></a>ログ ファイルの使用領域の最小化

**適用されます**Access 2013、Office 2013。

ログ ファイルがすぐにいっぱいことがあります (したがって、サーバーを停止する) 大量の SQL Server データベース上のアクティビティがある場合。 ログ ファイルを設定するには **[チェックポイント時の切り捨て**はデータベースのログ ファイルのライフ サイクルを大幅に拡張します。

**Microsoft SQL Server 6.5 でチェックポイント時のログの切り捨てを有効にするには**

1.  Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。

2.  この機能を有効にするデータベースの名前をダブルクリックします。

3.  [**データベース**] タブで、**削除**を選択します。

4.  **オプション**] タブから **[チェックポイント時のログの切り捨て]** を選択し、[ **OK**] をクリックします。

**Microsoft SQL Server 7.0 でチェックポイント時のログの切り捨てを有効にするには**

1.  Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベースのツリーを開きます。

2.  データベースにこの機能が有効になります、[**プロパティ**] の名前を右クリックします。

3.  **オプション**] タブから **[チェックポイント時のログの切り捨て]** を選択し、[ **OK**] をクリックします。

**チェックポイントの削除**機能の詳細については、Microsoft SQL Server のマニュアルを参照してください。

