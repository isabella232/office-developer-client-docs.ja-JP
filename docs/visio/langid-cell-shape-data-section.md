---
title: '[LangID] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: 図形データ値の記入に使用した言語を示します。
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805674"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="444a0-103">[LangID] セル ([図形データ] セクション)</span><span class="sxs-lookup"><span data-stu-id="444a0-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="444a0-104">図形データ値の記入に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="444a0-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="444a0-105">備考</span><span class="sxs-lookup"><span data-stu-id="444a0-105">Remarks</span></span>

<span data-ttu-id="444a0-106">Microsoft Office system のアプリケーションがサポートしている言語の一覧は、[[DocLangID]](doclangid-cell-document-properties-section.md) セル ([Document Properties] セクション) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="444a0-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="444a0-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="444a0-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="444a0-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="444a0-108">Cell name:</span></span>  <br/> | <span data-ttu-id="444a0-109">プロペラです。 *名*です。LangID でプロペラです。 *名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="444a0-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="444a0-110">プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="444a0-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="444a0-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="444a0-111">Section index:</span></span>  <br/> |<span data-ttu-id="444a0-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="444a0-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="444a0-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="444a0-113">Row index:</span></span>  <br/> |<span data-ttu-id="444a0-114">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="444a0-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="444a0-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="444a0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="444a0-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="444a0-116">**visCustPropsLangID**</span></span> <br/> |
   

