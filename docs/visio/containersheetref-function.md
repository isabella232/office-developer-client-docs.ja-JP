---
title: CONTAINERSHEETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: 図形を含む、指定されたコンテナーのシート参照を返します。
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318985"
---
# <a name="containersheetref-function"></a><span data-ttu-id="3c10b-103">CONTAINERSHEETREF 関数</span><span class="sxs-lookup"><span data-stu-id="3c10b-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="3c10b-104">図形を含む、指定されたコンテナーのシート参照を返します。</span><span class="sxs-lookup"><span data-stu-id="3c10b-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="3c10b-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="3c10b-105">Version Information</span></span>

<span data-ttu-id="3c10b-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="3c10b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3c10b-107">構文</span><span class="sxs-lookup"><span data-stu-id="3c10b-107">Syntax</span></span>

<span data-ttu-id="3c10b-108">CONTAINERSHEETREF (\* \* *index* \* \* \* \* *[, category]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3c10b-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3c10b-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c10b-109">Parameters</span></span>

|<span data-ttu-id="3c10b-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="3c10b-110">**Name**</span></span>|<span data-ttu-id="3c10b-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3c10b-111">**Required/Optional**</span></span>|<span data-ttu-id="3c10b-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3c10b-112">**Data Type**</span></span>|<span data-ttu-id="3c10b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c10b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3c10b-114">_index_</span><span class="sxs-lookup"><span data-stu-id="3c10b-114">_index_</span></span> <br/> |<span data-ttu-id="3c10b-115">必須</span><span class="sxs-lookup"><span data-stu-id="3c10b-115">Required</span></span>  <br/> |<span data-ttu-id="3c10b-116">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="3c10b-116">**Integer**</span></span> <br/> |<span data-ttu-id="3c10b-117">コンテナーの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3c10b-117">The 1-based index of the container.</span></span> <span data-ttu-id="3c10b-118">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c10b-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="3c10b-119">_項目_</span><span class="sxs-lookup"><span data-stu-id="3c10b-119">_category_</span></span> <br/> |<span data-ttu-id="3c10b-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c10b-120">Optional</span></span>  <br/> |<span data-ttu-id="3c10b-121">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="3c10b-121">**String**</span></span> <br/> |<span data-ttu-id="3c10b-122">コンテナーのカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="3c10b-122">The category of the container.</span></span> <span data-ttu-id="3c10b-123">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c10b-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3c10b-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="3c10b-124">Return value</span></span>

<span data-ttu-id="3c10b-125">シェイプシート参照</span><span class="sxs-lookup"><span data-stu-id="3c10b-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c10b-126">解説</span><span class="sxs-lookup"><span data-stu-id="3c10b-126">Remarks</span></span>

<span data-ttu-id="3c10b-127">コンテナーの Z オーダー (前面から背面) を基に計算されるコンテナーのインデックス。</span><span class="sxs-lookup"><span data-stu-id="3c10b-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="3c10b-128">*カテゴリ*は、図形の分類に使用できるユーザー定義の文字列です。</span><span class="sxs-lookup"><span data-stu-id="3c10b-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="3c10b-129">カテゴリは、図形のシェイプシート内の User.msvShapeCategories セルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="3c10b-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="3c10b-130">1 つの図形に対して複数のカテゴリを定義するには、カテゴリをセミコロンで区切ります。</span><span class="sxs-lookup"><span data-stu-id="3c10b-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="3c10b-131">図形がコンテナーのメンバーではない場合、または指定されたインデックス番号とカテゴリの両方に一致するコンテナーがない場合、CONTAINERSHEETREF は #REF! を返します。</span><span class="sxs-lookup"><span data-stu-id="3c10b-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="3c10b-132">例</span><span class="sxs-lookup"><span data-stu-id="3c10b-132">Example</span></span>

<span data-ttu-id="3c10b-133">CONTAINERSHEETREF (1)!寸法</span><span class="sxs-lookup"><span data-stu-id="3c10b-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="3c10b-134">図形が属しているページの最前面にあるコンテナーの [Height] セルの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3c10b-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

