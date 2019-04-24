---
title: '[LangID] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: テキストの記入に使用した言語を示します。
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326923"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="b0e9e-103">[LangID] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="b0e9e-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="b0e9e-104">テキストの記入に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="b0e9e-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b0e9e-105">解説</span><span class="sxs-lookup"><span data-stu-id="b0e9e-105">Remarks</span></span>

<span data-ttu-id="b0e9e-106">Microsoft Office アプリケーションがサポートしている言語の一覧は、[[DocLangID](doclangid-cell-document-properties-section.md)] セル ([Document Properties] セクション) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0e9e-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="b0e9e-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LangID] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0e9e-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0e9e-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="b0e9e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b0e9e-109"><1> [ *i* ]、 *i* =、2、3...</span><span class="sxs-lookup"><span data-stu-id="b0e9e-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b0e9e-110">プログラムから、インデックスによって [LangID] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b0e9e-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0e9e-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b0e9e-111">Section index:</span></span>  <br/> |<span data-ttu-id="b0e9e-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b0e9e-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="b0e9e-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b0e9e-113">Row index:</span></span>  <br/> |<span data-ttu-id="b0e9e-114">**visRowCharacter** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="b0e9e-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b0e9e-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b0e9e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b0e9e-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="b0e9e-116">**visCharacterLangID**</span></span> <br/> |
   

