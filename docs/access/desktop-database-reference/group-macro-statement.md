---
title: Group マクロ ステートメント
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713997"
---
# <a name="group-macro-statement"></a><span data-ttu-id="839ec-102">Group マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="839ec-102">Group macro statement</span></span>


<span data-ttu-id="839ec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="839ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="839ec-104">**Group** ステートメントでは、マクロ内で展開または折りたたみできるアクションのブロックを指定できます。</span><span class="sxs-lookup"><span data-stu-id="839ec-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="839ec-105">設定</span><span class="sxs-lookup"><span data-stu-id="839ec-105">Setting</span></span>

<span data-ttu-id="839ec-106">**Group** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="839ec-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="839ec-107">引数</span><span class="sxs-lookup"><span data-stu-id="839ec-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="839ec-108">必須</span><span class="sxs-lookup"><span data-stu-id="839ec-108">Required</span></span></p></th>
<th><p><span data-ttu-id="839ec-109">説明</span><span class="sxs-lookup"><span data-stu-id="839ec-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="839ec-110"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="839ec-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="839ec-111">いいえ</span><span class="sxs-lookup"><span data-stu-id="839ec-111">No</span></span></p></td>
<td><p><span data-ttu-id="839ec-112">折りたたんだときに、グループのタイトルとして表示する文字列。</span><span class="sxs-lookup"><span data-stu-id="839ec-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="839ec-113">注釈</span><span class="sxs-lookup"><span data-stu-id="839ec-113">Remarks</span></span>

<span data-ttu-id="839ec-114">**グループ**・ ステートメントでは、個別に実行できるマクロの領域が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="839ec-114">The **Group** statment does not define a region of a macro that can be executed separately.</span></span> <span data-ttu-id="839ec-115">**[サブマクロ](submacro-macro-statement.md)** ステートメントを使用すると、**マクロ デザイナー** ] ウィンドウで個別に実行するアクションのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="839ec-115">Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

