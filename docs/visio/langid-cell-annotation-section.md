---
title: '[LangID] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: コメントの記入に使用した言語を示します。
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360551"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="669d6-103">[LangID] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="669d6-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="669d6-104">コメントの記入に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="669d6-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="669d6-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。</span><span class="sxs-lookup"><span data-stu-id="669d6-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="669d6-106">これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="669d6-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="669d6-107">解説</span><span class="sxs-lookup"><span data-stu-id="669d6-107">Remarks</span></span>

<span data-ttu-id="669d6-p102">この値は、コメントを記入したときに言語バーでアクティブになっている言語のロケール ID (LCID) です。Microsoft Office のアプリケーションがサポートしている言語の一覧は、[[DocLangID](doclangid-cell-document-properties-section.md)] セル ([Document Properties] セクション) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="669d6-p102">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered. For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="669d6-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="669d6-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="669d6-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="669d6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="669d6-112"><1> [ *i* ]: *i* =、2、3...</span><span class="sxs-lookup"><span data-stu-id="669d6-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="669d6-113">プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="669d6-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="669d6-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="669d6-114">Section index:</span></span>  <br/> |<span data-ttu-id="669d6-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="669d6-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="669d6-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="669d6-116">Row index:</span></span>  <br/> |<span data-ttu-id="669d6-117">**visRowAnnotation** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="669d6-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="669d6-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="669d6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="669d6-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="669d6-119">**visAnnotationLangID**</span></span> <br/> |
   

