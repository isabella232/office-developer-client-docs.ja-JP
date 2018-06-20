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
description: 検索ボックスに指定したキーワードを使用して HTML ヘルプ ファイルを開きます。
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805522"
---
# <a name="help-function"></a><span data-ttu-id="6add7-103">HELP 関数</span><span class="sxs-lookup"><span data-stu-id="6add7-103">HELP Function</span></span>

<span data-ttu-id="6add7-104">**検索**ボックスに指定した*キーワード*では、HTML ヘルプ ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6add7-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6add7-105">構文</span><span class="sxs-lookup"><span data-stu-id="6add7-105">Syntax</span></span>

<span data-ttu-id="6add7-106">ヘルプ ("* * *filename.chm!keyword* * *")</span><span class="sxs-lookup"><span data-stu-id="6add7-106">HELP(" ** *filename.chm!keyword* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6add7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6add7-107">Parameters</span></span>

|<span data-ttu-id="6add7-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6add7-108">**Name**</span></span>|<span data-ttu-id="6add7-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6add7-109">**Required/Optional**</span></span>|<span data-ttu-id="6add7-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6add7-110">**Data Type**</span></span>|<span data-ttu-id="6add7-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6add7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6add7-112">_filename.chm!keyword_</span><span class="sxs-lookup"><span data-stu-id="6add7-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="6add7-113">必須</span><span class="sxs-lookup"><span data-stu-id="6add7-113">Required</span></span>  <br/> |<span data-ttu-id="6add7-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6add7-114">**String**</span></span> <br/> | <span data-ttu-id="6add7-115">ヘルプ ファイルの名前と検索対象のキーワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="6add7-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6add7-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6add7-116">Remarks</span></span>

<span data-ttu-id="6add7-117">*キーワード*が指定されていない場合、ヘルプ機能は、ヘルプ ファイルの目次のページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6add7-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6add7-118">例</span><span class="sxs-lookup"><span data-stu-id="6add7-118">Example</span></span>

<span data-ttu-id="6add7-119">HELP("visio.chm!shapesheet")</span><span class="sxs-lookup"><span data-stu-id="6add7-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="6add7-120">Visio ヘルプ ファイルを開き、キーワード "shapesheet" を含むトピックの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="6add7-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

