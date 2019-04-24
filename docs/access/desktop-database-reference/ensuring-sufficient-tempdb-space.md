---
title: 十分な TempDB 領域の確保
TOCTitle: Ensuring sufficient TempDB space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6414c9dd4c3218c2c2bf90f39d0cfb950e6e1018
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293575"
---
# <a name="ensuring-sufficient-tempdb-space"></a>十分な TempDB 領域の確保


**適用先:** Access 2013、Office 2013

Microsoft SQL Server 6.5 において処理領域が必要な [Recordset](recordset-object-ado.md) オブジェクトを処理している際にエラーが発生した場合は、TempDB のサイズを増やす必要があります (一部のクエリは、一時的な処理領域を必要とします。たとえば、ORDER BY 句のあるクエリでは **Recordset** のソートが必要ですが、これには一時的な処理領域が必要です)。

> [!IMPORTANT]
> [!重要] 一度展開したデバイスは簡単には圧縮できないので、実行前に以下の手順をよく読んでください。

> [!NOTE]
> [!メモ] 既定では、Microsoft SQL Server 7.0 以降のバージョンでは、TempDB は必要に応じて自動的に拡大できるように設定されます。したがって、この手順が必要なのは、7.0 より前のバージョンを実行するサーバーだけです。



**SQL Server 6.5 の TempDB 領域を拡大するには**

1.  Microsoft SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイスのツリーを開きます。

2.  Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.

3.  In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).

4.  [すぐに変更] をクリックして、論理 TempDB の拡張可能領域を増やします。

5.  サーバーのデータベース ツリーを開き、[TempDB] をダブルクリックして [データベースの編集] ダイアログ ボックスを開きます。[データベース] タブには、TempDB に現在割り当てられている領域の大きさ ([データ サイズ]) が表示されます。既定では、この大きさは 2 MB です。

6.  Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.

7.  Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.

8.  Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.

このトピックの詳細については、Microsoft SQL Server Enterprise Manager ヘルプの「データベースのサイズを拡張する方法」を参照してください。

