---
title: '[Name] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: 図面校閲者の名前が含まれます。
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417687"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="8d720-103">[Name] セル ([Reviewer] セクション)</span><span class="sxs-lookup"><span data-stu-id="8d720-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="8d720-104">図面校閲者の名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d720-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d720-105">注釈</span><span class="sxs-lookup"><span data-stu-id="8d720-105">Remarks</span></span>

 <span data-ttu-id="8d720-106">この値の既定値は、[ **Visio のオプション**] ダイアログボックス ([**ファイル**] タブをクリックし、[**オプション**] をクリックし、[**全般**] をクリック) の [**全般**] タブの [**ユーザー名**] ボックスにある名前です。</span><span class="sxs-lookup"><span data-stu-id="8d720-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="8d720-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [name] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d720-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d720-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="8d720-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8d720-109">Reviewer.Name [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="8d720-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8d720-110">プログラムから、インデックスによって [Name] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d720-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d720-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8d720-111">Section index:</span></span>  <br/> |<span data-ttu-id="8d720-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="8d720-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="8d720-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8d720-113">Row index:</span></span>  <br/> |<span data-ttu-id="8d720-114">**visRowReviewer** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="8d720-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8d720-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8d720-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8d720-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="8d720-116">**visReviewerName**</span></span> <br/> |
   

