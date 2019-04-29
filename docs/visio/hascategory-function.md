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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433354"
---
# <a name="hascategory-function"></a><span data-ttu-id="21f02-103">HASCATEGORY 関数</span><span class="sxs-lookup"><span data-stu-id="21f02-103">HASCATEGORY Function</span></span>

<span data-ttu-id="21f02-104">指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="21f02-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="21f02-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="21f02-105">Version Information</span></span>

<span data-ttu-id="21f02-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="21f02-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="21f02-107">構文</span><span class="sxs-lookup"><span data-stu-id="21f02-107">Syntax</span></span>

<span data-ttu-id="21f02-108">hascategory (\* \* *category* \* \*)</span><span class="sxs-lookup"><span data-stu-id="21f02-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21f02-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21f02-109">Parameters</span></span>

|<span data-ttu-id="21f02-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="21f02-110">**Name**</span></span>|<span data-ttu-id="21f02-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="21f02-111">**Required/Optional**</span></span>|<span data-ttu-id="21f02-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="21f02-112">**Data Type**</span></span>|<span data-ttu-id="21f02-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="21f02-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21f02-114">_項目_</span><span class="sxs-lookup"><span data-stu-id="21f02-114">_category_</span></span> <br/> |<span data-ttu-id="21f02-115">必須</span><span class="sxs-lookup"><span data-stu-id="21f02-115">Required</span></span>  <br/> |<span data-ttu-id="21f02-116">**String**</span><span class="sxs-lookup"><span data-stu-id="21f02-116">**String**</span></span> <br/> |<span data-ttu-id="21f02-117">検索するカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="21f02-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="21f02-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="21f02-118">Return value</span></span>

 <span data-ttu-id="21f02-119">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="21f02-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21f02-120">注釈</span><span class="sxs-lookup"><span data-stu-id="21f02-120">Remarks</span></span>

 <span data-ttu-id="21f02-121">*カテゴリ*は、図形の分類に使用できるユーザー定義の文字列です。</span><span class="sxs-lookup"><span data-stu-id="21f02-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="21f02-122">カテゴリは、図形のシェイプシート内の User.msvShapeCategories セルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="21f02-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="21f02-123">1 つの図形に対して複数のカテゴリを定義するには、カテゴリをセミコロンで区切ります。</span><span class="sxs-lookup"><span data-stu-id="21f02-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

