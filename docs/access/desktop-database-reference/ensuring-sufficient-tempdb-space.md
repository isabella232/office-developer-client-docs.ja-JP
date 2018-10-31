---
title: TempDB 用に十分な空き領域を確保する
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d049a098a7f7cfd826c6c5945c71831acbceb04
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863053"
---
# <a name="ensuring-sufficient-tempdb-space"></a>TempDB 用に十分な空き領域を確保する


**適用されます**Access 2013 |。Office 2013

Microsoft SQL Server 6.5 において処理領域が必要な [Recordset](recordset-object-ado.md) オブジェクトを処理している際にエラーが発生した場合は、TempDB のサイズを増やす必要があります (一部のクエリは、一時的な処理領域を必要とします。たとえば、ORDER BY 句のあるクエリでは **Recordset** のソートが必要ですが、これには一時的な処理領域が必要です)。

> [!IMPORTANT]
> [!重要] 一度展開したデバイスは簡単には圧縮できないので、実行前に以下の手順をよく読んでください。

> [!NOTE]
> [!メモ] 既定では、Microsoft SQL Server 7.0 以降のバージョンでは、TempDB は必要に応じて自動的に拡大できるように設定されます。したがって、この手順が必要なのは、7.0 より前のバージョンを実行するサーバーだけです。



**SQL Server 6.5 の TempDB 領域を拡大するには**

1.  Microsoft® SQL Server Enterprise Manager を起動し、サーバーのツリーを開き、次にデータベース デバイス ツリーを開きます。

2.  マスターなどの拡張を (物理的な) デバイスを選択し、デバイスを開くには、[**データベース デバイスの編集**] ダイアログ ボックスをダブルクリックします。 このダイアログ ボックスは、現在のデータベースを使用している容量を表示します。

3.  [**サイズ**] ボックスで、指定したサイズ (たとえば、50 メガバイト (MB) のハード_ディスクの空き領域) のデバイスを向上します。

4.  **すぐに変更**する (論理) の TempDB の拡張可能領域の量を増やす] をクリックします。

5.  サーバーのデータベース ツリーを開き、 **TempDB** **データベースの編集**] ダイアログ ボックスを開く] をダブルクリックします。 [**データベース**] タブには、(**データのサイズ**) を TempDB に現在割り当てられている領域の容量が一覧表示されます。 既定では、これは、2 MB です。

6.  [**サイズ**] グループで、[**展開**を] をクリックします。 グラフでは、各物理デバイスで使用できる割り当て領域を示しています。 茶色のバーは、使用可能な領域を表します。

7.  などの**ログ デバイス****のサイズ (MB)** ] ボックスで利用可能なサイズを表示するのには、マスター シェイプを選択します。

8.  **すぐに拡張**領域を TempDB データベースを割り当てる] をクリックします。 **データベースの編集**] ダイアログ ボックスでは、TempDB に新規に割り当てられたサイズが表示されます。

このトピックの詳細については、Microsoft SQL Server Enterprise Manager ヘルプの「データベースのサイズを拡張する方法」を参照してください。

