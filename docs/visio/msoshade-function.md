---
title: MSOSHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: 指定された割合で明度を減らして色を変更します。
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414495"
---
# <a name="msoshade-function"></a><span data-ttu-id="d3aff-103">MSOSHADE 関数</span><span class="sxs-lookup"><span data-stu-id="d3aff-103">MSOSHADE Function</span></span>

<span data-ttu-id="d3aff-104">指定された割合で明度を減らして色を変更します。</span><span class="sxs-lookup"><span data-stu-id="d3aff-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d3aff-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="d3aff-105">Version Information</span></span>

<span data-ttu-id="d3aff-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d3aff-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d3aff-107">構文</span><span class="sxs-lookup"><span data-stu-id="d3aff-107">Syntax</span></span>

<span data-ttu-id="d3aff-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d3aff-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d3aff-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d3aff-109">Parameters</span></span>

|<span data-ttu-id="d3aff-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="d3aff-110">**Name**</span></span>|<span data-ttu-id="d3aff-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d3aff-111">**Required/Optional**</span></span>|<span data-ttu-id="d3aff-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d3aff-112">**Data Type**</span></span>|<span data-ttu-id="d3aff-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="d3aff-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d3aff-114">_color_</span><span class="sxs-lookup"><span data-stu-id="d3aff-114">_color_</span></span> <br/> |<span data-ttu-id="d3aff-115">必須</span><span class="sxs-lookup"><span data-stu-id="d3aff-115">Required</span></span>  <br/> |<span data-ttu-id="d3aff-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="d3aff-116">**RGB**</span></span> <br/> |<span data-ttu-id="d3aff-117">標準の RGB (red、green、blue) による色の値または色への参照。</span><span class="sxs-lookup"><span data-stu-id="d3aff-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="d3aff-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="d3aff-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="d3aff-119">必須</span><span class="sxs-lookup"><span data-stu-id="d3aff-119">Required</span></span>  <br/> |<span data-ttu-id="d3aff-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="d3aff-120">**Integer**</span></span> <br/> |<span data-ttu-id="d3aff-121">白に向かって変化する割合 (-100%)または黒 (100%)色の  _値から取得_ します。</span><span class="sxs-lookup"><span data-stu-id="d3aff-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3aff-122">注釈</span><span class="sxs-lookup"><span data-stu-id="d3aff-122">Remarks</span></span>

<span data-ttu-id="d3aff-123">色の値  _が_ 白または黒に近いほど、特定の -deltaLum 値によって生成される網掛け  _への変更が小さ_ になります。</span><span class="sxs-lookup"><span data-stu-id="d3aff-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

