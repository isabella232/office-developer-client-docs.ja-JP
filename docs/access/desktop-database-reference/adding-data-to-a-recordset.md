---
title: レコードセットにデータを追加する
TOCTitle: Adding Data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42cdf33d7b34dc4a48392d21dcdb2d9de26b4bbc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477707"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="85b0c-102">レコードセットにデータを追加する</span><span class="sxs-lookup"><span data-stu-id="85b0c-102">Adding Data to a Recordset</span></span>


<span data-ttu-id="85b0c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="85b0c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="85b0c-p101">**Recordset** は、最も頻繁に使用される ADO オブジェクトであると言えます。ADO における **Recordset** は、データ ソースから取得した結果セットと、それに関連付けられたカーソルの動作の組み合わせであると考えてください。このため、データを **Recordset** に追加した後、 **Recordset** のメソッドとプロパティを使用して、データ行の移動、行に含まれる値の表示、および結果セットに対するその他の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="85b0c-p101">The **Recordset** is probably the most used of the ADO objects. In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors. Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="85b0c-p102">このセクションでは、 **Recordset** にデータを追加する方法を説明します。データ間の移動、およびデータの更新については、「 [4 章: データを編集する](chapter-4-editing-data.md)」、および「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。 **Recordset** に結果セットを追加するために、 **Command** オブジェクトの高度な機能を必ず使用する必要はありません。多くの場合、 **Recordset** の **Source** プロパティを設定するか、 **Recordset** オブジェクトの **Open** メソッドにコマンドを渡すことにより、コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="85b0c-p102">This section will focus on adding data to the **Recordset**. For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md). You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**. Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="85b0c-p103">データ ソースから **Recordset** にデータを追加するには、さまざまな方法があります。どの手法を使用するかは、アプリケーションの要件、およびプロバイダーの機能によって異なります。</span><span class="sxs-lookup"><span data-stu-id="85b0c-p103">There are a variety of ways to add data from your data source to a **Recordset**. The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

