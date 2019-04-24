---
title: PLAYSOUND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: サウンドファイルまたはシステムサウンドを再生します。
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346845"
---
# <a name="playsound-function"></a><span data-ttu-id="9f725-103">PLAYSOUND 関数</span><span class="sxs-lookup"><span data-stu-id="9f725-103">PLAYSOUND Function</span></span>

<span data-ttu-id="9f725-104">サウンドファイルまたはシステムサウンドを再生します。</span><span class="sxs-lookup"><span data-stu-id="9f725-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f725-105">構文</span><span class="sxs-lookup"><span data-stu-id="9f725-105">Syntax</span></span>

<span data-ttu-id="9f725-106">PLAYSOUND ("\* \* *filename* \* *" | "* **エイリアス** \*", \* \* *isalias* \* \*, \* \* *beep* \* \*, \* \* *synch* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9f725-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f725-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9f725-107">Parameters</span></span>

|<span data-ttu-id="9f725-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="9f725-108">**Name**</span></span>|<span data-ttu-id="9f725-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9f725-109">**Required/Optional**</span></span>|<span data-ttu-id="9f725-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9f725-110">**Data Type**</span></span>|<span data-ttu-id="9f725-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9f725-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f725-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="9f725-112">_filename_</span></span> <br/> |<span data-ttu-id="9f725-113">必須</span><span class="sxs-lookup"><span data-stu-id="9f725-113">Required</span></span>  <br/> |<span data-ttu-id="9f725-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9f725-114">**String**</span></span> <br/> |<span data-ttu-id="9f725-115">再生するサウンド ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f725-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="9f725-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="9f725-116">_alias_</span></span> <br/> |<span data-ttu-id="9f725-117">必須</span><span class="sxs-lookup"><span data-stu-id="9f725-117">Required</span></span>  <br/> |<span data-ttu-id="9f725-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9f725-118">**String**</span></span> <br/> | <span data-ttu-id="9f725-119">エイリアスが示すシステム サウンドを指定します。</span><span class="sxs-lookup"><span data-stu-id="9f725-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="9f725-120">_isalias_</span><span class="sxs-lookup"><span data-stu-id="9f725-120">_isAlias_</span></span> <br/> |<span data-ttu-id="9f725-121">必須</span><span class="sxs-lookup"><span data-stu-id="9f725-121">Required</span></span>  <br/> |<span data-ttu-id="9f725-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f725-122">**Boolean**</span></span> <br/> | <span data-ttu-id="9f725-123">直前の式 (引数) がエイリアスまたはファイル名のどちらであるかを指定します。エイリアスを指定するには、ゼロ以外の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9f725-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="9f725-124">_鳴り_</span><span class="sxs-lookup"><span data-stu-id="9f725-124">_beep_</span></span> <br/> |<span data-ttu-id="9f725-125">必須</span><span class="sxs-lookup"><span data-stu-id="9f725-125">Required</span></span>  <br/> |<span data-ttu-id="9f725-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f725-126">**Boolean**</span></span> <br/> |<span data-ttu-id="9f725-127">サウンドを再生できない場合にビープ音を鳴らすかどうかを指定します。ビープ音を鳴らすには、ゼロ以外の数値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9f725-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="9f725-128">_とれ_</span><span class="sxs-lookup"><span data-stu-id="9f725-128">_synch_</span></span> <br/> |<span data-ttu-id="9f725-129">必須</span><span class="sxs-lookup"><span data-stu-id="9f725-129">Required</span></span>  <br/> |<span data-ttu-id="9f725-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f725-130">**Boolean**</span></span> <br/> |<span data-ttu-id="9f725-131">非同期 (0) または同期 (1) のどちらでサウンドを再生するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9f725-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f725-132">解説</span><span class="sxs-lookup"><span data-stu-id="9f725-132">Remarks</span></span>

<span data-ttu-id="9f725-133">通常、サウンドを再生している間に Visio が処理を続行できるように、サウンドを非同期で再生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f725-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="9f725-134">複数のサウンドを文字列でつなぎ合わせるには、それらを同時に再生するか、再生に失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="9f725-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9f725-135">例 1</span><span class="sxs-lookup"><span data-stu-id="9f725-135">Example 1</span></span>

<span data-ttu-id="9f725-136">PLAYSOUND("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9f725-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="9f725-137">ウェーブ オーディオ ファイル chord.wav を非同期で実行し、警告のビープ音を鳴らしません。</span><span class="sxs-lookup"><span data-stu-id="9f725-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9f725-138">例 2</span><span class="sxs-lookup"><span data-stu-id="9f725-138">Example 2</span></span>

<span data-ttu-id="9f725-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9f725-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="9f725-140">システムのメッセージ (警告) サウンドを非同期で実行し、警告のビープ音を鳴らしません。</span><span class="sxs-lookup"><span data-stu-id="9f725-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

