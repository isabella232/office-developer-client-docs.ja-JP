---
title: '[Prompt] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。 アプリケーションでは、プロンプトのテキストがテキスト文字列であることを示すには引用符 () で自動的に囲まれます。 等号 (=) を入力して引用符を省略した場合は、このアプリケーションを評価するセルの数式を入力することができます。
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806126"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="70c02-105">[Prompt] セル ([User-Defined Cells] セクション)</span><span class="sxs-lookup"><span data-stu-id="70c02-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="70c02-p102">ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。プロンプト テキストは自動的に引用符 (" ") で囲まれ、テキスト文字列として認識されます。このセルに数式を入力するには、等号 (=) を入力して引用符を省略します。これにより、数式はアプリケーションによって評価されます。</span><span class="sxs-lookup"><span data-stu-id="70c02-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70c02-109">備考</span><span class="sxs-lookup"><span data-stu-id="70c02-109">Remarks</span></span>

<span data-ttu-id="70c02-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Prompt] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="70c02-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70c02-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="70c02-111">Cell name:</span></span>  <br/> | <span data-ttu-id="70c02-112">ユーザーです。</span><span class="sxs-lookup"><span data-stu-id="70c02-112">User.</span></span>  <span data-ttu-id="70c02-113">*名*です。プロンプトの場所のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="70c02-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="70c02-114">*名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="70c02-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="70c02-115">プログラムから、インデックスによって [Prompt] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="70c02-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70c02-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="70c02-116">Section index:</span></span>  <br/> |<span data-ttu-id="70c02-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="70c02-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="70c02-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="70c02-118">Row index:</span></span>  <br/> |<span data-ttu-id="70c02-119">**visRowUser +***i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="70c02-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="70c02-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="70c02-120">Cell index:</span></span>  <br/> |<span data-ttu-id="70c02-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="70c02-121">**visUserPrompt**</span></span> <br/> |
   

