---
title: HASCATEGORY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: 指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805519"
---
# <a name="hascategory-function"></a><span data-ttu-id="2995b-103">HASCATEGORY 関数</span><span class="sxs-lookup"><span data-stu-id="2995b-103">HASCATEGORY Function</span></span>

<span data-ttu-id="2995b-104">指定した文字列が図形のカテゴリの一覧にある場合は、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="2995b-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="2995b-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="2995b-105">Version Information</span></span>

<span data-ttu-id="2995b-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="2995b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2995b-107">構文</span><span class="sxs-lookup"><span data-stu-id="2995b-107">Syntax</span></span>

<span data-ttu-id="2995b-108">HASCATEGORY (* **カテゴリ** *)</span><span class="sxs-lookup"><span data-stu-id="2995b-108">HASCATEGORY(** *category* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2995b-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="2995b-109">Parameters</span></span>

|<span data-ttu-id="2995b-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="2995b-110">**Name**</span></span>|<span data-ttu-id="2995b-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="2995b-111">**Required/Optional**</span></span>|<span data-ttu-id="2995b-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="2995b-112">**Data Type**</span></span>|<span data-ttu-id="2995b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="2995b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2995b-114">_category_</span><span class="sxs-lookup"><span data-stu-id="2995b-114">_category_</span></span> <br/> |<span data-ttu-id="2995b-115">必須</span><span class="sxs-lookup"><span data-stu-id="2995b-115">Required</span></span>  <br/> |<span data-ttu-id="2995b-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="2995b-116">**String**</span></span> <br/> |<span data-ttu-id="2995b-117">検索するカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="2995b-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2995b-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2995b-118">Return value</span></span>

 <span data-ttu-id="2995b-119">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="2995b-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2995b-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="2995b-120">Remarks</span></span>

 <span data-ttu-id="2995b-121">*カテゴリ*は、図形を分類するために使用できるユーザー定義の文字列です。</span><span class="sxs-lookup"><span data-stu-id="2995b-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="2995b-122">User.msvShapeCategories 図形のシェイプ シート セルでは、カテゴリを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2995b-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="2995b-123">カテゴリをセミコロンで区切ると、図形の複数のカテゴリを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2995b-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

