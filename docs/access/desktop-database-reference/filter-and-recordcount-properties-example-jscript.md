---
title: Filter プロパティと RecordCount プロパティの使用例 (JScript)
TOCTitle: Filter and RecordCount properties example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d5994a072e34d07256cbce7b45ffe3fd5179f99
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877605"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a><span data-ttu-id="f1b49-102">Filter プロパティと RecordCount プロパティの使用例 (JScript)</span><span class="sxs-lookup"><span data-stu-id="f1b49-102">Filter and RecordCount properties example (JScript)</span></span>


<span data-ttu-id="f1b49-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f1b49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1b49-104">この例では、Northwind データベースの Companies テーブルの **Recordset** を開き、 [Filter](filter-property-ado.md) プロパティを使って、表示されるレコードを、CompanyName フィールドが文字 D で始まるレコードに制限します。次のコードをコピーし、メモ帳またはその他のテキスト エディターに貼り付けて **FilterJS.asp** という名前で保存してください。</span><span class="sxs-lookup"><span data-stu-id="f1b49-104">This example opens a **Recordset** on the Companies table of the Northwind database and then uses the [Filter](filter-property-ado.md) property to limit the records visible to those where the CompanyName field starts with the letter D. Cut and paste the following code to Notepad or another text editor, and save it as **FilterJS.asp**.</span></span>

