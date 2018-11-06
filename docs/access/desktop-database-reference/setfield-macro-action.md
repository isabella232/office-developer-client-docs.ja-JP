---
title: SetField マクロ アクション
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66dfe95aaa335e14b0148d2fcd610abc30556e3a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997498"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="df6eb-102">SetField マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="df6eb-102">SetField macro action</span></span>

<span data-ttu-id="df6eb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="df6eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df6eb-104">" **SetField** /フィールドの設定" アクションを使用すると、フィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="df6eb-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="df6eb-105">[!メモ] " **SetField** /フィールドの設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="df6eb-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="df6eb-106">設定</span><span class="sxs-lookup"><span data-stu-id="df6eb-106">Setting</span></span>

<span data-ttu-id="df6eb-107">" **SetField** /フィールドの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df6eb-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df6eb-108">引数</span><span class="sxs-lookup"><span data-stu-id="df6eb-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="df6eb-109">説明</span><span class="sxs-lookup"><span data-stu-id="df6eb-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df6eb-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="df6eb-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="df6eb-111">フィールドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="df6eb-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df6eb-112"><strong>値</strong></span><span class="sxs-lookup"><span data-stu-id="df6eb-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="df6eb-113">フィールドに割り当てる値を指定する式。</span><span class="sxs-lookup"><span data-stu-id="df6eb-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="df6eb-114">備考</span><span class="sxs-lookup"><span data-stu-id="df6eb-114">Remarks</span></span>

<span data-ttu-id="df6eb-115">**SetField**アクションは、 **[CreateRecord](createrecord-data-block.md)** または**[EditRecord](editrecord-data-block.md)** のデータ ブロックの外部では使用できません。</span><span class="sxs-lookup"><span data-stu-id="df6eb-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

