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
description: ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。 アプリケーションは、テキスト文字列であることを示すために、プロンプトテキストを二重引用符 () で自動的に囲みます。 等号 (=) を入力し、引用符を省略した場合、このセルにはアプリケーションが評価する数式を入力できます。
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435727"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="e6eda-105">[Prompt] セル ([User-Defined Cells] セクション)</span><span class="sxs-lookup"><span data-stu-id="e6eda-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="e6eda-p102">ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。プロンプト テキストは自動的に引用符 (" ") で囲まれ、テキスト文字列として認識されます。このセルに数式を入力するには、等号 (=) を入力して引用符を省略します。これにより、数式はアプリケーションによって評価されます。</span><span class="sxs-lookup"><span data-stu-id="e6eda-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6eda-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e6eda-109">Remarks</span></span>

<span data-ttu-id="e6eda-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Prompt] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e6eda-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6eda-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="e6eda-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e6eda-112">マニュアル.</span><span class="sxs-lookup"><span data-stu-id="e6eda-112">User.</span></span>  <span data-ttu-id="e6eda-113">*名前*です。ユーザーにプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="e6eda-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="e6eda-114">*name*には、行の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6eda-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="e6eda-115">プログラムから、インデックスによって [Prompt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6eda-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6eda-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6eda-116">Section index:</span></span>  <br/> |<span data-ttu-id="e6eda-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="e6eda-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="e6eda-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6eda-118">Row index:</span></span>  <br/> |<span data-ttu-id="e6eda-119">\*\*visRowUser +\*\*\*\* i = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="e6eda-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e6eda-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6eda-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e6eda-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="e6eda-121">**visUserPrompt**</span></span> <br/> |
   

