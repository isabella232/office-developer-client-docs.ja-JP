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
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805651"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="72507-103">[LangID] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="72507-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="72507-104">テキストの記入に使用した言語を示します。</span><span class="sxs-lookup"><span data-stu-id="72507-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="72507-105">備考</span><span class="sxs-lookup"><span data-stu-id="72507-105">Remarks</span></span>

<span data-ttu-id="72507-106">Microsoft Office アプリケーションでサポートされる言語のリストは、 [[doclangid]](doclangid-cell-document-properties-section.md)セル ([ドキュメント プロパティ] セクションで) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72507-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="72507-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって langid] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="72507-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72507-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="72507-108">Cell name:</span></span>  <br/> | <span data-ttu-id="72507-109">Char.LangID [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="72507-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="72507-110">プログラムから、インデックスによって [langid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="72507-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72507-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="72507-111">Section index:</span></span>  <br/> |<span data-ttu-id="72507-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="72507-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="72507-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="72507-113">Row index:</span></span>  <br/> |<span data-ttu-id="72507-114">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="72507-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="72507-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="72507-115">Cell index:</span></span>  <br/> |<span data-ttu-id="72507-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="72507-116">**visCharacterLangID**</span></span> <br/> |
   

