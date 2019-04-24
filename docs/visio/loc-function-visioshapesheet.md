---
title: LOC 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: 1つの図形のローカル座標で定義された点を取得し、式に関連付けられている図形のローカル座標で表される等価の点を返します。
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344430"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="51777-103">LOC 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="51777-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="51777-104">1つの図形のローカル座標で定義された点を取得し、式に関連付けられている図形のローカル座標で表される等価の点を返します。</span><span class="sxs-lookup"><span data-stu-id="51777-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51777-105">構文</span><span class="sxs-lookup"><span data-stu-id="51777-105">Syntax</span></span>

<span data-ttu-id="51777-106">LOC (\* \* *point* \* \*)</span><span class="sxs-lookup"><span data-stu-id="51777-106">LOC(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51777-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="51777-107">Parameters</span></span>

|<span data-ttu-id="51777-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="51777-108">**Name**</span></span>|<span data-ttu-id="51777-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="51777-109">**Required/Optional**</span></span>|<span data-ttu-id="51777-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="51777-110">**Data Type**</span></span>|<span data-ttu-id="51777-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="51777-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51777-112">_ポイント_</span><span class="sxs-lookup"><span data-stu-id="51777-112">_point_</span></span> <br/> |<span data-ttu-id="51777-113">必須</span><span class="sxs-lookup"><span data-stu-id="51777-113">Required</span></span>  <br/> |<span data-ttu-id="51777-114">**String**</span><span class="sxs-lookup"><span data-stu-id="51777-114">**String**</span></span> <br/> | <span data-ttu-id="51777-115">1 つの図形のローカル座標に定義されている点を指定します。</span><span class="sxs-lookup"><span data-stu-id="51777-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51777-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="51777-116">Return value</span></span>

<span data-ttu-id="51777-117">文字列</span><span class="sxs-lookup"><span data-stu-id="51777-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51777-118">注釈</span><span class="sxs-lookup"><span data-stu-id="51777-118">Remarks</span></span>

<span data-ttu-id="51777-p101">ローカル座標は図形の選択範囲の左下隅から測定されます。両方の図形は、同じページになければなりません。</span><span class="sxs-lookup"><span data-stu-id="51777-p101">Local coordinates are measured from the lower-left corner of the shape's selection rectangle. Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="51777-121">例</span><span class="sxs-lookup"><span data-stu-id="51777-121">Example</span></span>

<span data-ttu-id="51777-122">LOC (PNT (Sheet. 5![locpinx]、Sheet[locpiny]))</span><span class="sxs-lookup"><span data-stu-id="51777-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="51777-p102">この式では、PNT 関数が Sheet.5 にある一連のローカル座標を点に変換します (Sheet.5 は同じ図面ページ上にある別の図形です)。次に LOC 関数は、この点を、現在の図形のローカル座標系で相当する点に変換します。このとき、現在の図形の選択範囲の左下隅を原点として変換が行われます。</span><span class="sxs-lookup"><span data-stu-id="51777-p102">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point. (Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="51777-125">Sheet.5 の 5 は図形の ID 番号であり、これは [**図形の名前**] ダイアログ ボックス ([**開発者用**] タブ) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="51777-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

