---
title: SetField マクロ アクション
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ca2315a9a84000aa29b88043e4edea05ffb0ea
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922826"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="c3cdd-102">SetField マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="c3cdd-102">SetField macro action</span></span>


<span data-ttu-id="c3cdd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3cdd-104">" **SetField** /フィールドの設定" アクションを使用すると、フィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c3cdd-105">[!メモ] " <STRONG>SetField</STRONG> /フィールドの設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="c3cdd-106">設定</span><span class="sxs-lookup"><span data-stu-id="c3cdd-106">Setting</span></span>

<span data-ttu-id="c3cdd-107">" **SetField** /フィールドの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3cdd-108">引数</span><span class="sxs-lookup"><span data-stu-id="c3cdd-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="c3cdd-109">説明</span><span class="sxs-lookup"><span data-stu-id="c3cdd-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3cdd-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="c3cdd-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cdd-111">フィールドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3cdd-112"><strong>値</strong></span><span class="sxs-lookup"><span data-stu-id="c3cdd-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="c3cdd-113">フィールドに割り当てる値を指定する式。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c3cdd-114">備考</span><span class="sxs-lookup"><span data-stu-id="c3cdd-114">Remarks</span></span>

<span data-ttu-id="c3cdd-115">**SetField**アクションは、 **[CreateRecord](createrecord-data-block.md)** または**[EditRecord](editrecord-data-block.md)** のデータ ブロックの外部では使用できません。</span><span class="sxs-lookup"><span data-stu-id="c3cdd-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

