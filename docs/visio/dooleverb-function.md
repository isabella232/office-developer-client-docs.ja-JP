---
title: DOOLEVERB 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: OLE オブジェクトの動詞を実行します。
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435663"
---
# <a name="dooleverb-function"></a><span data-ttu-id="5ca68-103">DOOLEVERB 関数</span><span class="sxs-lookup"><span data-stu-id="5ca68-103">DOOLEVERB Function</span></span>

<span data-ttu-id="5ca68-104">OLE オブジェクトの動詞を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ca68-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5ca68-105">構文</span><span class="sxs-lookup"><span data-stu-id="5ca68-105">Syntax</span></span>

<span data-ttu-id="5ca68-106">DOOLEVERB(" \*\* *verb* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="5ca68-106">DOOLEVERB(" \*\* *verb* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ca68-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ca68-107">Parameters</span></span>

|<span data-ttu-id="5ca68-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5ca68-108">**Name**</span></span>|<span data-ttu-id="5ca68-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5ca68-109">**Required/Optional**</span></span>|<span data-ttu-id="5ca68-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5ca68-110">**Data Type**</span></span>|<span data-ttu-id="5ca68-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ca68-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ca68-112">_"verb"_</span><span class="sxs-lookup"><span data-stu-id="5ca68-112">_"verb"_</span></span> <br/> |<span data-ttu-id="5ca68-113">必須</span><span class="sxs-lookup"><span data-stu-id="5ca68-113">Required</span></span>  <br/> |<span data-ttu-id="5ca68-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5ca68-114">**String**</span></span> <br/> |<span data-ttu-id="5ca68-115">実行する動詞を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ca68-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ca68-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5ca68-116">Remarks</span></span>

<span data-ttu-id="5ca68-p101">以前のバージョンの Visio では、この関数は _DOOLEVERB に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ca68-p101">In earlier versions of Visio, this function appears as _DOOLEVERB. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5ca68-119">例</span><span class="sxs-lookup"><span data-stu-id="5ca68-119">Example</span></span>

<span data-ttu-id="5ca68-120">DOOLEVERB("edit")</span><span class="sxs-lookup"><span data-stu-id="5ca68-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="5ca68-121">OLE オブジェクト プログラムを実行し、リンクされた、または埋め込まれているオブジェクトを表示して編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5ca68-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

