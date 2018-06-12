---
title: PATHSEGMENT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: 指定したパスに沿って指定した割合のマークで 1 ベースのセグメント数を返します。
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805986"
---
# <a name="pathsegment-function"></a><span data-ttu-id="acc5c-103">PATHSEGMENT 関数</span><span class="sxs-lookup"><span data-stu-id="acc5c-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="acc5c-104">指定したパスに沿って指定した割合のマークで 1 ベースのセグメント数を返します。</span><span class="sxs-lookup"><span data-stu-id="acc5c-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="acc5c-105">構文</span><span class="sxs-lookup"><span data-stu-id="acc5c-105">Syntax</span></span>

<span data-ttu-id="acc5c-106">PATHSEGMENT (* **で** *、* **旅行** *)</span><span class="sxs-lookup"><span data-stu-id="acc5c-106">PATHSEGMENT(** *section* **, ** *travel* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="acc5c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="acc5c-107">Parameters</span></span>

|<span data-ttu-id="acc5c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="acc5c-108">**Name**</span></span>|<span data-ttu-id="acc5c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="acc5c-109">**Required/Optional**</span></span>|<span data-ttu-id="acc5c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="acc5c-110">**Data Type**</span></span>|<span data-ttu-id="acc5c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="acc5c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="acc5c-112">_section_</span><span class="sxs-lookup"><span data-stu-id="acc5c-112">_section_</span></span> <br/> |<span data-ttu-id="acc5c-113">必須</span><span class="sxs-lookup"><span data-stu-id="acc5c-113">Required</span></span>  <br/> |<span data-ttu-id="acc5c-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="acc5c-114">**String**</span></span> <br/> |<span data-ttu-id="acc5c-115">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="acc5c-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="acc5c-116">_旅行_</span><span class="sxs-lookup"><span data-stu-id="acc5c-116">_travel_</span></span> <br/> |<span data-ttu-id="acc5c-117">必須</span><span class="sxs-lookup"><span data-stu-id="acc5c-117">Required</span></span>  <br/> |<span data-ttu-id="acc5c-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="acc5c-118">**Double**</span></span> <br/> |<span data-ttu-id="acc5c-p101">スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acc5c-p101">The percentage of the path traversed, from the begin point to the end point. Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="acc5c-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="acc5c-121">Return value</span></span>

<span data-ttu-id="acc5c-122">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="acc5c-122">Integer</span></span>
  

