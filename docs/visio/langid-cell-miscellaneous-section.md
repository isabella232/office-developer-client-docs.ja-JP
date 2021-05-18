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
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406676"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="2e9ad-103">[LangID] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="2e9ad-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="2e9ad-104">セル数式の作成に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="2e9ad-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2e9ad-105">注釈</span><span class="sxs-lookup"><span data-stu-id="2e9ad-105">Remarks</span></span>

<span data-ttu-id="2e9ad-106">Microsoft Office アプリケーションがサポートしている言語の一覧は、[[DocLangID](doclangid-cell-document-properties-section.md)] セル ([Document Properties] セクション) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e9ad-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="2e9ad-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2e9ad-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e9ad-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="2e9ad-108">Cell name:</span></span>  <br/> | <span data-ttu-id="2e9ad-109">LangID</span><span class="sxs-lookup"><span data-stu-id="2e9ad-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="2e9ad-110">プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e9ad-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e9ad-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2e9ad-111">Section index:</span></span>  <br/> |<span data-ttu-id="2e9ad-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e9ad-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e9ad-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2e9ad-113">Row index:</span></span>  <br/> |<span data-ttu-id="2e9ad-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="2e9ad-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="2e9ad-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2e9ad-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2e9ad-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="2e9ad-116">**visObjLangID**</span></span> <br/> |
   

