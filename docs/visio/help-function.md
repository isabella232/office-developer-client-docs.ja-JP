---
title: HELP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: 検索ボックスに、指定したキーワードを含む HTML ヘルプファイルを開きます。
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431338"
---
# <a name="help-function"></a><span data-ttu-id="95fcf-103">HELP 関数</span><span class="sxs-lookup"><span data-stu-id="95fcf-103">HELP Function</span></span>

<span data-ttu-id="95fcf-104">**検索**ボックスに、指定した*キーワード*を含む HTML ヘルプファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="95fcf-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="95fcf-105">構文</span><span class="sxs-lookup"><span data-stu-id="95fcf-105">Syntax</span></span>

<span data-ttu-id="95fcf-106">ヘルプ ("\* **ファイル名 .chm! キーワード** \*")</span><span class="sxs-lookup"><span data-stu-id="95fcf-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95fcf-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="95fcf-107">Parameters</span></span>

|<span data-ttu-id="95fcf-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="95fcf-108">**Name**</span></span>|<span data-ttu-id="95fcf-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="95fcf-109">**Required/Optional**</span></span>|<span data-ttu-id="95fcf-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="95fcf-110">**Data Type**</span></span>|<span data-ttu-id="95fcf-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="95fcf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95fcf-112">_ファイル名 .chm! キーワード_</span><span class="sxs-lookup"><span data-stu-id="95fcf-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="95fcf-113">必須</span><span class="sxs-lookup"><span data-stu-id="95fcf-113">Required</span></span>  <br/> |<span data-ttu-id="95fcf-114">**String**</span><span class="sxs-lookup"><span data-stu-id="95fcf-114">**String**</span></span> <br/> | <span data-ttu-id="95fcf-115">ヘルプ ファイルの名前と検索対象のキーワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="95fcf-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95fcf-116">注釈</span><span class="sxs-lookup"><span data-stu-id="95fcf-116">Remarks</span></span>

<span data-ttu-id="95fcf-117">*キーワード*が指定されていない場合、help 関数は、ヘルプファイルの [コンテンツ] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="95fcf-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="95fcf-118">例</span><span class="sxs-lookup"><span data-stu-id="95fcf-118">Example</span></span>

<span data-ttu-id="95fcf-119">ヘルプ ("visio. .chm! シェイプシート")</span><span class="sxs-lookup"><span data-stu-id="95fcf-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="95fcf-120">Visio ヘルプ ファイルを開き、キーワード "shapesheet" を含むトピックの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="95fcf-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

