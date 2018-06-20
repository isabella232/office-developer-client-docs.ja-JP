---
title: '[LangID] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: セル数式の作成に使用した言語を示します。
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805694"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="59556-103">[LangID] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="59556-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="59556-104">セル数式の作成に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="59556-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="59556-105">備考</span><span class="sxs-lookup"><span data-stu-id="59556-105">Remarks</span></span>

<span data-ttu-id="59556-106">Microsoft Office アプリケーションでサポートされる言語のリストは、 [[doclangid]](doclangid-cell-document-properties-section.md)セル ([ドキュメント プロパティ] セクションで) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59556-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="59556-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって langid] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="59556-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59556-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="59556-108">Cell name:</span></span>  <br/> | <span data-ttu-id="59556-109">LangID</span><span class="sxs-lookup"><span data-stu-id="59556-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="59556-110">プログラムから、インデックスによって [langid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="59556-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59556-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="59556-111">Section index:</span></span>  <br/> |<span data-ttu-id="59556-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59556-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="59556-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="59556-113">Row index:</span></span>  <br/> |<span data-ttu-id="59556-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="59556-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="59556-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="59556-115">Cell index:</span></span>  <br/> |<span data-ttu-id="59556-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="59556-116">**visObjLangID**</span></span> <br/> |
   

