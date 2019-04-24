---
title: Filter プロパティと RecordCount プロパティの使用例 (JScript)
TOCTitle: Filter and RecordCount properties example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 993209478d18d013771de8239d8e8cd10efc5da2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292490"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a><span data-ttu-id="cac42-102">Filter プロパティと RecordCount プロパティの使用例 (JScript)</span><span class="sxs-lookup"><span data-stu-id="cac42-102">Filter and RecordCount properties example (JScript)</span></span>


<span data-ttu-id="cac42-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="cac42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cac42-104">この例では、Northwind データベースの Companies テーブルの **Recordset** を開き、 [Filter](filter-property-ado.md) プロパティを使って、表示されるレコードを、CompanyName フィールドが文字 D で始まるレコードに制限します。次のコードをコピーし、メモ帳またはその他のテキスト エディターに貼り付けて **FilterJS.asp** という名前で保存してください。</span><span class="sxs-lookup"><span data-stu-id="cac42-104">This example opens a **Recordset** on the Companies table of the Northwind database and then uses the [Filter](filter-property-ado.md) property to limit the records visible to those where the CompanyName field starts with the letter D. Cut and paste the following code to Notepad or another text editor, and save it as **FilterJS.asp**.</span></span>

