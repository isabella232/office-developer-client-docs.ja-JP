---
title: HASCATEGORY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: 指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360166"
---
# <a name="hascategory-function"></a><span data-ttu-id="1f3a9-103">HASCATEGORY 関数</span><span class="sxs-lookup"><span data-stu-id="1f3a9-103">HASCATEGORY Function</span></span>

<span data-ttu-id="1f3a9-104">指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="1f3a9-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="1f3a9-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="1f3a9-105">Version Information</span></span>

<span data-ttu-id="1f3a9-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="1f3a9-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1f3a9-107">構文</span><span class="sxs-lookup"><span data-stu-id="1f3a9-107">Syntax</span></span>

<span data-ttu-id="1f3a9-108">hascategory (\* \* *category* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1f3a9-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1f3a9-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1f3a9-109">Parameters</span></span>

|<span data-ttu-id="1f3a9-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="1f3a9-110">**Name**</span></span>|<span data-ttu-id="1f3a9-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="1f3a9-111">**Required/Optional**</span></span>|<span data-ttu-id="1f3a9-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="1f3a9-112">**Data Type**</span></span>|<span data-ttu-id="1f3a9-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="1f3a9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1f3a9-114">_項目_</span><span class="sxs-lookup"><span data-stu-id="1f3a9-114">_category_</span></span> <br/> |<span data-ttu-id="1f3a9-115">必須</span><span class="sxs-lookup"><span data-stu-id="1f3a9-115">Required</span></span>  <br/> |<span data-ttu-id="1f3a9-116">**String**</span><span class="sxs-lookup"><span data-stu-id="1f3a9-116">**String**</span></span> <br/> |<span data-ttu-id="1f3a9-117">検索するカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="1f3a9-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1f3a9-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="1f3a9-118">Return value</span></span>

 <span data-ttu-id="1f3a9-119">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="1f3a9-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f3a9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="1f3a9-120">Remarks</span></span>

 <span data-ttu-id="1f3a9-121">*カテゴリ*は、図形の分類に使用できるユーザー定義の文字列です。</span><span class="sxs-lookup"><span data-stu-id="1f3a9-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="1f3a9-122">カテゴリは、図形のシェイプシート内の User.msvShapeCategories セルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="1f3a9-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="1f3a9-123">1 つの図形に対して複数のカテゴリを定義するには、カテゴリをセミコロンで区切ります。</span><span class="sxs-lookup"><span data-stu-id="1f3a9-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

