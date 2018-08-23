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
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="6f920-103">[LangID] セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="6f920-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="6f920-104">セル数式の作成に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="6f920-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6f920-105">備考</span><span class="sxs-lookup"><span data-stu-id="6f920-105">Remarks</span></span>

<span data-ttu-id="6f920-106">Microsoft Office アプリケーションがサポートしている言語の一覧は、[[DocLangID](doclangid-cell-document-properties-section.md)] セル ([Document Properties] セクション) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f920-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="6f920-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f920-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f920-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="6f920-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6f920-109">LangID</span><span class="sxs-lookup"><span data-stu-id="6f920-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="6f920-110">プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6f920-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f920-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6f920-111">Section index:</span></span>  <br/> |<span data-ttu-id="6f920-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f920-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6f920-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6f920-113">Row index:</span></span>  <br/> |<span data-ttu-id="6f920-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6f920-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="6f920-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6f920-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6f920-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="6f920-116">**visObjLangID**</span></span> <br/> |
   

