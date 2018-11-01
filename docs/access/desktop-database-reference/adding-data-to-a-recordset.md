---
title: レコードセットにデータを追加する
TOCTitle: Adding Data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b013ab0b05242b4928f7a9b9d974ef98ca6103d0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885025"
---
# <a name="adding-data-to-a-recordset"></a>レコードセットへのデータの追加


**適用されます**Access 2013、Office 2013。

**Recordset** は、最も頻繁に使用される ADO オブジェクトであると言えます。ADO における **Recordset** は、データ ソースから取得した結果セットと、それに関連付けられたカーソルの動作の組み合わせであると考えてください。このため、データを **Recordset** に追加した後、 **Recordset** のメソッドとプロパティを使用して、データ行の移動、行に含まれる値の表示、および結果セットに対するその他の操作を実行できます。

このセクションでは、 **Recordset** にデータを追加する方法を説明します。データ間の移動、およびデータの更新については、「 [4 章: データを編集する](chapter-4-editing-data.md)」、および「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。 **Recordset** に結果セットを追加するために、 **Command** オブジェクトの高度な機能を必ず使用する必要はありません。多くの場合、 **Recordset** の **Source** プロパティを設定するか、 **Recordset** オブジェクトの **Open** メソッドにコマンドを渡すことにより、コマンドを実行できます。

データ ソースから **Recordset** にデータを追加するには、さまざまな方法があります。どの手法を使用するかは、アプリケーションの要件、およびプロバイダーの機能によって異なります。

