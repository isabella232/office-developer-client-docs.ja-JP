---
title: ソートプロパティ (ADOX)
TOCTitle: SortOrder property (ADOX)
ms:assetid: c2b8c84d-acc4-9929-fff5-9a088abbfcf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249951(v=office.15)
ms:contentKeyID: 48547557
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 735e72e8ed4f06c887ff790209529787e38142a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306441"
---
# <a name="sortorder-property-adox"></a><span data-ttu-id="545c5-102">ソートプロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="545c5-102">SortOrder property (ADOX)</span></span>


<span data-ttu-id="545c5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="545c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="545c5-104">列の並べ替え順序を示します (インデックス列のみ)。</span><span class="sxs-lookup"><span data-stu-id="545c5-104">Indicates the sort sequence for the column (index columns only).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="545c5-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="545c5-105">Settings and return values</span></span>

<span data-ttu-id="545c5-106">**SortOrderEnum** 定数の 1 つである長整数型 ( [Long](sortorderenum.md) ) の値を設定および取得します。</span><span class="sxs-lookup"><span data-stu-id="545c5-106">Sets and returns a **Long** value that can be one of the [SortOrderEnum](sortorderenum.md) constants.</span></span> <span data-ttu-id="545c5-107">既定値は **adSortAscending** です。</span><span class="sxs-lookup"><span data-stu-id="545c5-107">The default value is **adSortAscending**.</span></span>

## <a name="remarks"></a><span data-ttu-id="545c5-108">注釈</span><span class="sxs-lookup"><span data-stu-id="545c5-108">Remarks</span></span>

<span data-ttu-id="545c5-109">このプロパティは、[Index](index-object-adox.md) の [Columns](columns-collection-adox.md) コレクションにある [Column](column-object-adox.md) オブジェクトのみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="545c5-109">This property only applies to [Column](column-object-adox.md) objects in the [Columns](columns-collection-adox.md) collection of an [Index](index-object-adox.md).</span></span>

