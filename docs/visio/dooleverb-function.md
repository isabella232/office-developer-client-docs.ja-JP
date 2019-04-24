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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301492"
---
# <a name="dooleverb-function"></a><span data-ttu-id="d9a20-103">DOOLEVERB 関数</span><span class="sxs-lookup"><span data-stu-id="d9a20-103">DOOLEVERB Function</span></span>

<span data-ttu-id="d9a20-104">OLE オブジェクトの動詞を実行します。</span><span class="sxs-lookup"><span data-stu-id="d9a20-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d9a20-105">構文</span><span class="sxs-lookup"><span data-stu-id="d9a20-105">Syntax</span></span>

<span data-ttu-id="d9a20-106">DOOLEVERB ("\* \* *verb* \* \*")</span><span class="sxs-lookup"><span data-stu-id="d9a20-106">DOOLEVERB(" \*\* *verb* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d9a20-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9a20-107">Parameters</span></span>

|<span data-ttu-id="d9a20-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d9a20-108">**Name**</span></span>|<span data-ttu-id="d9a20-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d9a20-109">**Required/Optional**</span></span>|<span data-ttu-id="d9a20-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d9a20-110">**Data Type**</span></span>|<span data-ttu-id="d9a20-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9a20-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d9a20-112">_xexch50_</span><span class="sxs-lookup"><span data-stu-id="d9a20-112">_"verb"_</span></span> <br/> |<span data-ttu-id="d9a20-113">必須</span><span class="sxs-lookup"><span data-stu-id="d9a20-113">Required</span></span>  <br/> |<span data-ttu-id="d9a20-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d9a20-114">**String**</span></span> <br/> |<span data-ttu-id="d9a20-115">実行する動詞を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9a20-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9a20-116">解説</span><span class="sxs-lookup"><span data-stu-id="d9a20-116">Remarks</span></span>

<span data-ttu-id="d9a20-p101">以前のバージョンの Visio では、この関数は _DOOLEVERB に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9a20-p101">In earlier versions of Visio, this function appears as _DOOLEVERB. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d9a20-119">例</span><span class="sxs-lookup"><span data-stu-id="d9a20-119">Example</span></span>

<span data-ttu-id="d9a20-120">DOOLEVERB ("edit")</span><span class="sxs-lookup"><span data-stu-id="d9a20-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="d9a20-121">OLE オブジェクト プログラムを実行し、リンクされた、または埋め込まれているオブジェクトを表示して編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d9a20-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

