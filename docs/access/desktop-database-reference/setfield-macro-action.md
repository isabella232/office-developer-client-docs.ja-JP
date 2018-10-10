---
title: "\"SetField/フィールドの設定\" マクロ アクション"
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7050065ccb42d5e6cc9347f32df056891f4ed078
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478516"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="f4c1c-102">"SetField/フィールドの設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="f4c1c-102">SetField Macro Action</span></span>


<span data-ttu-id="f4c1c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4c1c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4c1c-104">" **SetField** /フィールドの設定" アクションを使用すると、フィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f4c1c-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f4c1c-105">[!メモ] " <STRONG>SetField</STRONG> /フィールドの設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4c1c-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="f4c1c-106">設定</span><span class="sxs-lookup"><span data-stu-id="f4c1c-106">Setting</span></span>

<span data-ttu-id="f4c1c-107">" **SetField** /フィールドの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f4c1c-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4c1c-108">引数</span><span class="sxs-lookup"><span data-stu-id="f4c1c-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="f4c1c-109">説明</span><span class="sxs-lookup"><span data-stu-id="f4c1c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4c1c-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="f4c1c-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c1c-111">フィールドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="f4c1c-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c1c-112"><strong>値</strong></span><span class="sxs-lookup"><span data-stu-id="f4c1c-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="f4c1c-113">フィールドに割り当てる値を指定する式。</span><span class="sxs-lookup"><span data-stu-id="f4c1c-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f4c1c-114">備考</span><span class="sxs-lookup"><span data-stu-id="f4c1c-114">Remarks</span></span>

<span data-ttu-id="f4c1c-115">**SetField**アクションは、 **[CreateRecord](createrecord-data-block.md)** または**[EditRecord](editrecord-data-block.md)** のデータ ブロックの外部では使用できません。</span><span class="sxs-lookup"><span data-stu-id="f4c1c-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

