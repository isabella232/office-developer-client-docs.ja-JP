---
title: SetField マクロ アクション
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722320"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="5af0a-102">SetField マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="5af0a-102">SetField macro action</span></span>

<span data-ttu-id="5af0a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5af0a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5af0a-104">" **SetField** /フィールドの設定" アクションを使用すると、フィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5af0a-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="5af0a-105">[!メモ] " **SetField** /フィールドの設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5af0a-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="5af0a-106">設定</span><span class="sxs-lookup"><span data-stu-id="5af0a-106">Setting</span></span>

<span data-ttu-id="5af0a-107">" **SetField** /フィールドの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5af0a-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5af0a-108">引数</span><span class="sxs-lookup"><span data-stu-id="5af0a-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="5af0a-109">説明</span><span class="sxs-lookup"><span data-stu-id="5af0a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5af0a-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="5af0a-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5af0a-111">フィールドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="5af0a-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af0a-112"><strong>値</strong></span><span class="sxs-lookup"><span data-stu-id="5af0a-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="5af0a-113">フィールドに割り当てる値を指定する式。</span><span class="sxs-lookup"><span data-stu-id="5af0a-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5af0a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5af0a-114">Remarks</span></span>

<span data-ttu-id="5af0a-115">**SetField**アクションは、 **[CreateRecord](createrecord-data-block.md)** または**[EditRecord](editrecord-data-block.md)** のデータ ブロックの外部では使用できません。</span><span class="sxs-lookup"><span data-stu-id="5af0a-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

