---
title: MSOTINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: 指定した割合で明度を増やして色を変更します。
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805940"
---
# <a name="msotint-function"></a><span data-ttu-id="e55be-103">MSOTINT 関数</span><span class="sxs-lookup"><span data-stu-id="e55be-103">MSOTINT Function</span></span>

<span data-ttu-id="e55be-104">指定した割合で明度を増やして色を変更します。</span><span class="sxs-lookup"><span data-stu-id="e55be-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e55be-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="e55be-105">Version Information</span></span>

<span data-ttu-id="e55be-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="e55be-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e55be-107">構文</span><span class="sxs-lookup"><span data-stu-id="e55be-107">Syntax</span></span>

<span data-ttu-id="e55be-108">MSOTINT (* **色** *、* * *deltaLum* * *)</span><span class="sxs-lookup"><span data-stu-id="e55be-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e55be-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="e55be-109">Parameters</span></span>

|<span data-ttu-id="e55be-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="e55be-110">**Name**</span></span>|<span data-ttu-id="e55be-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e55be-111">**Required/Optional**</span></span>|<span data-ttu-id="e55be-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e55be-112">**Data Type**</span></span>|<span data-ttu-id="e55be-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="e55be-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e55be-114">_color_</span><span class="sxs-lookup"><span data-stu-id="e55be-114">_color_</span></span> <br/> |<span data-ttu-id="e55be-115">必須</span><span class="sxs-lookup"><span data-stu-id="e55be-115">Required</span></span>  <br/> |<span data-ttu-id="e55be-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="e55be-116">**RGB**</span></span> <br/> |<span data-ttu-id="e55be-117">標準の RGB (red、green、blue) による色の値または色への参照。</span><span class="sxs-lookup"><span data-stu-id="e55be-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="e55be-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="e55be-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="e55be-119">必須</span><span class="sxs-lookup"><span data-stu-id="e55be-119">Required</span></span>  <br/> |<span data-ttu-id="e55be-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e55be-120">**Integer**</span></span> <br/> |<span data-ttu-id="e55be-121">白に向かって変化率 (-100%)] または [_色_の値から黒 (100%)。</span><span class="sxs-lookup"><span data-stu-id="e55be-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e55be-122">備考</span><span class="sxs-lookup"><span data-stu-id="e55be-122">Remarks</span></span>

<span data-ttu-id="e55be-123">近い_色_の値は、白または黒、小さな変更には特定の_deltaLum_の値によって生成される濃淡。</span><span class="sxs-lookup"><span data-stu-id="e55be-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

