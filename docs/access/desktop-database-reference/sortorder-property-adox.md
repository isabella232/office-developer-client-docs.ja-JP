---
title: SortOrder プロパティ (ADOX)
TOCTitle: SortOrder Property (ADOX)
ms:assetid: c2b8c84d-acc4-9929-fff5-9a088abbfcf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249951(v=office.15)
ms:contentKeyID: 48547557
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e17e160213eb4766c1ace8ac8afd0356dcf6bb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25890016"
---
# <a name="sortorder-property-adox"></a><span data-ttu-id="1dbf0-102">SortOrder プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1dbf0-102">SortOrder Property (ADOX)</span></span>


<span data-ttu-id="1dbf0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1dbf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1dbf0-104">列の並べ替え順序を示します (インデックス列のみ)。</span><span class="sxs-lookup"><span data-stu-id="1dbf0-104">Indicates the sort sequence for the column (index columns only).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1dbf0-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="1dbf0-105">Settings and return values</span></span>

<span data-ttu-id="1dbf0-p101">**SortOrderEnum** 定数の 1 つである長整数型 ( [Long](sortorderenum.md) ) の値を設定および取得します。既定値は **adSortAscending** です。</span><span class="sxs-lookup"><span data-stu-id="1dbf0-p101">Sets and returns a **Long** value that can be one of the [SortOrderEnum](sortorderenum.md) constants. The default value is **adSortAscending**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dbf0-108">解説</span><span class="sxs-lookup"><span data-stu-id="1dbf0-108">Remarks</span></span>

<span data-ttu-id="1dbf0-109">このプロパティは、[Index](column-object-adox.md) の [Columns](columns-collection-adox.md) コレクションにある [Column](index-object-adox.md) オブジェクトのみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1dbf0-109">This property only applies to [Column](column-object-adox.md) objects in the [Columns](columns-collection-adox.md) collection of an [Index](index-object-adox.md).</span></span>

