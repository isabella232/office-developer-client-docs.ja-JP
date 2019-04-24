---
title: '[NoCoauth] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: microsoft SharePoint 2013 サーバーまたは microsoft OneDrive に保存されているドキュメントを共同編集セッションで同時に複数の作成者が編集できるようにするかどうかを設定します。
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319440"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="407b7-103">[NoCoauth] セル ([ドキュメントのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="407b7-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="407b7-104">microsoft SharePoint 2013 サーバーまたは microsoft OneDrive に保存されているドキュメントを共同編集セッションで同時に複数の作成者が編集できるようにするかどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="407b7-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="407b7-105">**値**</span><span class="sxs-lookup"><span data-stu-id="407b7-105">**Value**</span></span>|<span data-ttu-id="407b7-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="407b7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="407b7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="407b7-107">TRUE</span></span>  <br/> |<span data-ttu-id="407b7-108">ドキュメントは共同編集できません。開かれると編集用にロックされます。</span><span class="sxs-lookup"><span data-stu-id="407b7-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="407b7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="407b7-109">FALSE</span></span>  <br/> |<span data-ttu-id="407b7-110">ドキュメントは共同編集できます。</span><span class="sxs-lookup"><span data-stu-id="407b7-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="407b7-111">解説</span><span class="sxs-lookup"><span data-stu-id="407b7-111">Remarks</span></span>

<span data-ttu-id="407b7-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**NoCoauth**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="407b7-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="407b7-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="407b7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="407b7-114">[nocoauth]</span><span class="sxs-lookup"><span data-stu-id="407b7-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="407b7-115">プログラムから、インデックスによって [**NoCoauth**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="407b7-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="407b7-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="407b7-116">Section index:</span></span>  <br/> |<span data-ttu-id="407b7-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="407b7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="407b7-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="407b7-118">Row index:</span></span>  <br/> |<span data-ttu-id="407b7-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="407b7-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="407b7-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="407b7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="407b7-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="407b7-121">**visDocNoCoauth**</span></span> <br/> |
   

