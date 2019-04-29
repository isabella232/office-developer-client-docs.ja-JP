---
title: '[User-defined Cells] 行 ([User-defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: ソリューションでのユーザー定義のセルに関する、値と説明プロンプトを格納します。図形には、ユーザー定義の [Value]/[Prompt] セルの各組み合わせに対して 1 つの [User-defined Cells] 行があります。
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420690"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a><span data-ttu-id="2bb4f-104">[User-defined Cells] 行 ([User-defined Cells] セクション)</span><span class="sxs-lookup"><span data-stu-id="2bb4f-104">User-defined Cells Row (User-defined Cells Section)</span></span>

<span data-ttu-id="2bb4f-p102">ソリューションでのユーザー定義のセルに関する、値と説明プロンプトを格納します。図形には、ユーザー定義の [Value]/[Prompt] セルの各組み合わせに対して 1 つの [User-defined Cells] 行があります。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-p102">Contains the value and descriptive prompt for any user-defined cells in your solution. A shape contains one User-defined Cells row for each user-defined Value/Prompt cell pair.</span></span>
  
<span data-ttu-id="2bb4f-107">[User-defined Cells] 行の名前は User.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-107">User-defined Cells rows are named User.</span></span> <span data-ttu-id="2bb4f-108">次のセルに*名前*とが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-108">*name*  and contain the following cells.</span></span> <span data-ttu-id="2bb4f-109">詳細については、各セルに関連する項目を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-109">For more details, see the specific cell topics.</span></span> 
  
|<span data-ttu-id="2bb4f-110">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2bb4f-110">**Cell**</span></span>|<span data-ttu-id="2bb4f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2bb4f-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2bb4f-112">値</span><span class="sxs-lookup"><span data-stu-id="2bb4f-112">Value</span></span>](value-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="2bb4f-113">対応するユーザー定義のセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-113">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |
|[<span data-ttu-id="2bb4f-114">Prompt</span><span class="sxs-lookup"><span data-stu-id="2bb4f-114">Prompt</span></span>](prompt-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="2bb4f-115">ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-115">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bb4f-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2bb4f-116">Remarks</span></span>

<span data-ttu-id="2bb4f-p104">ユーザー定義のセルは、他のセルやアドオンによって参照される、数式または定数の入力に使用できます。ユーザー定義のセルの値には可搬性があります。たとえば、ある図形が持つユーザー定義のセルを別の図形が参照していて、その図形を、同じユーザー定義のセルを持たない図形にコピーした場合、ユーザー定義のセルがコピー先の図形に追加されます。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-p104">User-defined cells can be used for entering formulas or constants that are referred to by other cells or add-ons. Values in user-defined cells are portable, that is, if a shape that refers to a user-defined cell in one shape is copied to another shape that does not have the same user-defined cell, the cell is added to the shape.</span></span>
  
 <span data-ttu-id="2bb4f-119">必要に応じて [User.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-119">You can add as many User.</span></span>  <span data-ttu-id="2bb4f-120">必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-120">*name*  rows as you need, assign meaningful names to the rows, and set cell values.</span></span> <span data-ttu-id="2bb4f-121">既存の [User-defined Cells] セクションに行を追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-121">To add a row to an existing User-defined Cells section, right-click a row and click **Insert Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="2bb4f-122">これらのセルを行名で参照できます。これは、シェイプシートウィンドウに赤いテキストで表示されます。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-122">You can reference these cells by their row name, which appears in a ShapeSheet window in red text.</span></span> <span data-ttu-id="2bb4f-123">わかりやすい名前をユーザーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-123">To assign meaningful names to User.</span></span> <span data-ttu-id="2bb4f-124">[*名前*] 行をクリックし、「 *offset* 」などの名前を入力します。たとえば、行名のユーザーオフセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-124">*name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset.</span></span> <span data-ttu-id="2bb4f-125">その後、ユーザーの Offset を使用して [prompt] セルを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-125">You can then reference the Prompt cell using User.Offset.Prompt.</span></span> 
  
<span data-ttu-id="2bb4f-126">入力する行名は、セクション内で一意の名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bb4f-126">The row name you enter must be unique within the section.</span></span>
  

