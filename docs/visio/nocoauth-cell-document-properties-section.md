---
title: '[NoCoauth] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Microsoft SharePoint 2013 のサーバーまたはマイクロソフトの OneDrive に格納されているドキュメントにことができます coauthoring のセッションで同時に複数の作成者によって編集かどうかを設定します。
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805925"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="f83f4-103">[NoCoauth] セル ([ドキュメントのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f83f4-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="f83f4-104">Microsoft SharePoint 2013 のサーバーまたはマイクロソフトの OneDrive に格納されているドキュメントにことができます coauthoring のセッションで同時に複数の作成者によって編集かどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="f83f4-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="f83f4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f83f4-105">**Value**</span></span>|<span data-ttu-id="f83f4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f83f4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f83f4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f83f4-107">TRUE</span></span>  <br/> |<span data-ttu-id="f83f4-108">ドキュメントは共同編集できません。開かれると編集用にロックされます。</span><span class="sxs-lookup"><span data-stu-id="f83f4-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="f83f4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f83f4-109">FALSE</span></span>  <br/> |<span data-ttu-id="f83f4-110">ドキュメントは共同編集できます。</span><span class="sxs-lookup"><span data-stu-id="f83f4-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f83f4-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="f83f4-111">Remarks</span></span>

<span data-ttu-id="f83f4-112">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **NoCoauth** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f83f4-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f83f4-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="f83f4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f83f4-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="f83f4-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="f83f4-115">プログラムから、インデックスによって [ **NoCoauth** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f83f4-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f83f4-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f83f4-116">Section index:</span></span>  <br/> |<span data-ttu-id="f83f4-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f83f4-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f83f4-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f83f4-118">Row index:</span></span>  <br/> |<span data-ttu-id="f83f4-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="f83f4-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="f83f4-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f83f4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f83f4-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="f83f4-121">**visDocNoCoauth**</span></span> <br/> |
   

