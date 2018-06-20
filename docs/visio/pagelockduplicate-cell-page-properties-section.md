---
title: '[PageLockDuplicate] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: ページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805958"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="ad177-103">[PageLockDuplicate] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="ad177-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="ad177-104">ページを複製できるかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="ad177-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad177-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="ad177-105">TRUE</span></span>  <br/> |<span data-ttu-id="ad177-106">ページのショートカット メニューと**Page.Duplicate**オートメーション メソッドの**重複**を両方とも無効ページのです。</span><span class="sxs-lookup"><span data-stu-id="ad177-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="ad177-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="ad177-107">FALSE</span></span>  <br/> |<span data-ttu-id="ad177-108">このページは複製できます。</span><span class="sxs-lookup"><span data-stu-id="ad177-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad177-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="ad177-109">Remarks</span></span>

<span data-ttu-id="ad177-110">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **PageLockDuplicate** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ad177-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad177-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="ad177-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ad177-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="ad177-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="ad177-113">プログラムから、インデックスによって [ **PageLockDuplicate** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad177-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad177-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ad177-114">Section index:</span></span>  <br/> |<span data-ttu-id="ad177-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad177-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad177-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ad177-116">Row index:</span></span>  <br/> |<span data-ttu-id="ad177-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ad177-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ad177-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ad177-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ad177-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="ad177-119">**visPageLockDuplicate**</span></span> <br/> |
   

