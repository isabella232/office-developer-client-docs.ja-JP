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
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805655"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="de2a6-103">[LangID] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="de2a6-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="de2a6-104">コメントの記入に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="de2a6-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de2a6-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de2a6-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="de2a6-106">Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="de2a6-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de2a6-107">備考</span><span class="sxs-lookup"><span data-stu-id="de2a6-107">Remarks</span></span>

<span data-ttu-id="de2a6-108">この値は、ロケール ID (LCID) のコメントが入力されたときに、言語バーでアクティブになっている言語です。</span><span class="sxs-lookup"><span data-stu-id="de2a6-108">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered.</span></span> <span data-ttu-id="de2a6-109">Microsoft Office アプリケーションでサポートされる言語のリストは、 [[doclangid]](doclangid-cell-document-properties-section.md)セル ([ドキュメント プロパティ] セクションで) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de2a6-109">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="de2a6-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって langid] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de2a6-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de2a6-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="de2a6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="de2a6-112">Annotation.LangID [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="de2a6-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="de2a6-113">プログラムから、インデックスによって [langid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="de2a6-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de2a6-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="de2a6-114">Section index:</span></span>  <br/> |<span data-ttu-id="de2a6-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="de2a6-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="de2a6-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="de2a6-116">Row index:</span></span>  <br/> |<span data-ttu-id="de2a6-117">**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="de2a6-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="de2a6-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="de2a6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="de2a6-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="de2a6-119">**visAnnotationLangID**</span></span> <br/> |
   

