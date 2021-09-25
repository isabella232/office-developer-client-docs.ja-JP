---
title: レコードセットへのデータの追加
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 45dd7e954a379f732481c7442b205e7fd0bdce6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594490"
---
# <a name="adding-data-to-a-recordset"></a>レコードセットへのデータの追加

**適用先**: Access 2013、Office 2013

**Recordset** は、最も頻繁に使用される ADO オブジェクトであると言えます。ADO における **Recordset** は、データ ソースから取得した結果セットと、それに関連付けられたカーソルの動作の組み合わせであると考えてください。このため、データを **Recordset** に追加した後、 **Recordset** のメソッドとプロパティを使用して、データ行の移動、行に含まれる値の表示、および結果セットに対するその他の操作を実行できます。

このセクションでは、 **Recordset** にデータを追加する方法を説明します。データ間の移動、およびデータの更新については、「 [4 章: データを編集する](chapter-4-editing-data.md)」、および「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。 **Recordset** に結果セットを追加するために、 **Command** オブジェクトの高度な機能を必ず使用する必要はありません。多くの場合、 **Recordset** の **Source** プロパティを設定するか、 **Recordset** オブジェクトの **Open** メソッドにコマンドを渡すことにより、コマンドを実行できます。

データ ソースから **Recordset** にデータを追加するには、さまざまな方法があります。どの手法を使用するかは、アプリケーションの要件、およびプロバイダーの機能によって異なります。

