---
title: Group マクロ ステートメント
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c82169ac430496587c6ebab5e439d70bc9319b5e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930890"
---
# <a name="group-macro-statement"></a><span data-ttu-id="4218b-102">Group マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="4218b-102">Group macro statement</span></span>


<span data-ttu-id="4218b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4218b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4218b-104">**Group** ステートメントでは、マクロ内で展開または折りたたみできるアクションのブロックを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4218b-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="4218b-105">設定</span><span class="sxs-lookup"><span data-stu-id="4218b-105">Setting</span></span>

<span data-ttu-id="4218b-106">**Group** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4218b-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4218b-107">引数</span><span class="sxs-lookup"><span data-stu-id="4218b-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="4218b-108">必須</span><span class="sxs-lookup"><span data-stu-id="4218b-108">Required</span></span></p></th>
<th><p><span data-ttu-id="4218b-109">説明</span><span class="sxs-lookup"><span data-stu-id="4218b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4218b-110"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="4218b-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="4218b-111">いいえ</span><span class="sxs-lookup"><span data-stu-id="4218b-111">No</span></span></p></td>
<td><p><span data-ttu-id="4218b-112">折りたたんだときに、グループのタイトルとして表示する文字列。</span><span class="sxs-lookup"><span data-stu-id="4218b-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4218b-113">備考</span><span class="sxs-lookup"><span data-stu-id="4218b-113">Remarks</span></span>

<span data-ttu-id="4218b-114">**グループ**・ ステートメントでは、個別に実行できるマクロの領域が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="4218b-114">The **Group** statment does not define a region of a macro that can be executed separately.</span></span> <span data-ttu-id="4218b-115">**[サブマクロ](submacro-macro-statement.md)** ステートメントを使用すると、**マクロ デザイナー** ] ウィンドウで個別に実行するアクションのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="4218b-115">Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

