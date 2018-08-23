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
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805261"
---
# <a name="dooleverb-function"></a><span data-ttu-id="88669-103">DOOLEVERB 関数</span><span class="sxs-lookup"><span data-stu-id="88669-103">DOOLEVERB Function</span></span>

<span data-ttu-id="88669-104">OLE オブジェクトの動詞を実行します。</span><span class="sxs-lookup"><span data-stu-id="88669-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="88669-105">構文</span><span class="sxs-lookup"><span data-stu-id="88669-105">Syntax</span></span>

<span data-ttu-id="88669-106">DOOLEVERB ("* **動詞** *")</span><span class="sxs-lookup"><span data-stu-id="88669-106">DOOLEVERB(" ** *verb* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88669-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="88669-107">Parameters</span></span>

|<span data-ttu-id="88669-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="88669-108">**Name**</span></span>|<span data-ttu-id="88669-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="88669-109">**Required/Optional**</span></span>|<span data-ttu-id="88669-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="88669-110">**Data Type**</span></span>|<span data-ttu-id="88669-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="88669-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88669-112">_「動詞」_</span><span class="sxs-lookup"><span data-stu-id="88669-112">_"verb"_</span></span> <br/> |<span data-ttu-id="88669-113">必須</span><span class="sxs-lookup"><span data-stu-id="88669-113">Required</span></span>  <br/> |<span data-ttu-id="88669-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="88669-114">**String**</span></span> <br/> |<span data-ttu-id="88669-115">実行する動詞を指定します。</span><span class="sxs-lookup"><span data-stu-id="88669-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88669-116">注釈</span><span class="sxs-lookup"><span data-stu-id="88669-116">Remarks</span></span>

<span data-ttu-id="88669-p101">以前のバージョンの Visio では、この関数は _DOOLEVERB に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="88669-p101">In earlier versions of Visio, this function appears as _DOOLEVERB. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="88669-119">例</span><span class="sxs-lookup"><span data-stu-id="88669-119">Example</span></span>

<span data-ttu-id="88669-120">DOOLEVERB("edit")</span><span class="sxs-lookup"><span data-stu-id="88669-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="88669-121">OLE オブジェクト プログラムを実行し、リンクされた、または埋め込まれているオブジェクトを表示して編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="88669-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

