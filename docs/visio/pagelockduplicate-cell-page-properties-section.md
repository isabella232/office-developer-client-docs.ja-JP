---
title: '[PageLockDuplicate] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: ページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425982"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="ca901-103">[PageLockDuplicate] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="ca901-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="ca901-104">ページを複製できるかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="ca901-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca901-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca901-105">TRUE</span></span>  <br/> |<span data-ttu-id="ca901-106">このページでは、ページのショートカット メニューの [**複製**] と、**Page.Duplicate** オートメーション メソッドはどちらも無効化されています。</span><span class="sxs-lookup"><span data-stu-id="ca901-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="ca901-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca901-107">FALSE</span></span>  <br/> |<span data-ttu-id="ca901-108">このページは複製できます。</span><span class="sxs-lookup"><span data-stu-id="ca901-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca901-109">注釈</span><span class="sxs-lookup"><span data-stu-id="ca901-109">Remarks</span></span>

<span data-ttu-id="ca901-110">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**PageLockDuplicate**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca901-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca901-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="ca901-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ca901-112">[pagelockduplicate]</span><span class="sxs-lookup"><span data-stu-id="ca901-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="ca901-113">プログラムから、インデックスによって [**PageLockDuplicate**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca901-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca901-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca901-114">Section index:</span></span>  <br/> |<span data-ttu-id="ca901-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca901-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ca901-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca901-116">Row index:</span></span>  <br/> |<span data-ttu-id="ca901-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ca901-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ca901-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca901-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ca901-119">**vispagelockduplicate**</span><span class="sxs-lookup"><span data-stu-id="ca901-119">**visPageLockDuplicate**</span></span> <br/> |
   

