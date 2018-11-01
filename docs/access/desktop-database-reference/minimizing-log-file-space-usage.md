---
title: ログファイルの使用領域を最小化する
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 119e4bc607296d1a68aef6f85d44f15718940b42
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25866986"
---
# <a name="minimizing-log-file-space-usage"></a>ログファイルの使用領域を最小化する


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

