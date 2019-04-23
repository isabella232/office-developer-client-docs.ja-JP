---
title: レコードセットへのデータの追加
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280217"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="e64d2-102">レコードセットへのデータの追加</span><span class="sxs-lookup"><span data-stu-id="e64d2-102">Adding data to a Recordset</span></span>

<span data-ttu-id="e64d2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e64d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e64d2-p101">**Recordset** は、最も頻繁に使用される ADO オブジェクトであると言えます。ADO における **Recordset** は、データ ソースから取得した結果セットと、それに関連付けられたカーソルの動作の組み合わせであると考えてください。このため、データを **Recordset** に追加した後、 **Recordset** のメソッドとプロパティを使用して、データ行の移動、行に含まれる値の表示、および結果セットに対するその他の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="e64d2-p101">The **Recordset** is probably the most used of the ADO objects. In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors. Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="e64d2-p102">このセクションでは、 **Recordset** にデータを追加する方法を説明します。データ間の移動、およびデータの更新については、「 [4 章: データを編集する](chapter-4-editing-data.md)」、および「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。 **Recordset** に結果セットを追加するために、 **Command** オブジェクトの高度な機能を必ず使用する必要はありません。多くの場合、 **Recordset** の **Source** プロパティを設定するか、 **Recordset** オブジェクトの **Open** メソッドにコマンドを渡すことにより、コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="e64d2-p102">This section will focus on adding data to the **Recordset**. For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md). You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**. Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="e64d2-p103">データ ソースから **Recordset** にデータを追加するには、さまざまな方法があります。どの手法を使用するかは、アプリケーションの要件、およびプロバイダーの機能によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e64d2-p103">There are a variety of ways to add data from your data source to a **Recordset**. The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

