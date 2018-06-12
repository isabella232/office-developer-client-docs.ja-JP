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
description: サウンド ファイルまたはシステム サウンドを再生します。
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806030"
---
# <a name="playsound-function"></a><span data-ttu-id="fbe1b-103">PLAYSOUND 関数</span><span class="sxs-lookup"><span data-stu-id="fbe1b-103">PLAYSOUND Function</span></span>

<span data-ttu-id="fbe1b-104">サウンド ファイルまたはシステム サウンドを再生します。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fbe1b-105">構文</span><span class="sxs-lookup"><span data-stu-id="fbe1b-105">Syntax</span></span>

<span data-ttu-id="fbe1b-106">PLAYSOUND ("* **ファイル名** *"|"* **エイリアス** *"、* * *isAlias* * *、* **ビープ音が** *、* **同期** *)</span><span class="sxs-lookup"><span data-stu-id="fbe1b-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fbe1b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="fbe1b-107">Parameters</span></span>

|<span data-ttu-id="fbe1b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-108">**Name**</span></span>|<span data-ttu-id="fbe1b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-109">**Required/Optional**</span></span>|<span data-ttu-id="fbe1b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-110">**Data Type**</span></span>|<span data-ttu-id="fbe1b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fbe1b-112">filename</span><span class="sxs-lookup"><span data-stu-id="fbe1b-112">_filename_</span></span> <br/> |<span data-ttu-id="fbe1b-113">必須</span><span class="sxs-lookup"><span data-stu-id="fbe1b-113">Required</span></span>  <br/> |<span data-ttu-id="fbe1b-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-114">**String**</span></span> <br/> |<span data-ttu-id="fbe1b-115">再生するサウンド ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="fbe1b-116">_エイリアス_</span><span class="sxs-lookup"><span data-stu-id="fbe1b-116">_alias_</span></span> <br/> |<span data-ttu-id="fbe1b-117">必須</span><span class="sxs-lookup"><span data-stu-id="fbe1b-117">Required</span></span>  <br/> |<span data-ttu-id="fbe1b-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-118">**String**</span></span> <br/> | <span data-ttu-id="fbe1b-119">エイリアスが示すシステム サウンドを指定します。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="fbe1b-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="fbe1b-120">_isAlias_</span></span> <br/> |<span data-ttu-id="fbe1b-121">必須</span><span class="sxs-lookup"><span data-stu-id="fbe1b-121">Required</span></span>  <br/> |<span data-ttu-id="fbe1b-122">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-122">**Boolean**</span></span> <br/> | <span data-ttu-id="fbe1b-123">直前の式 (引数) がエイリアスまたはファイル名のどちらであるかを指定します。エイリアスを指定するには、ゼロ以外の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="fbe1b-124">_ビープ音_</span><span class="sxs-lookup"><span data-stu-id="fbe1b-124">_beep_</span></span> <br/> |<span data-ttu-id="fbe1b-125">必須</span><span class="sxs-lookup"><span data-stu-id="fbe1b-125">Required</span></span>  <br/> |<span data-ttu-id="fbe1b-126">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-126">**Boolean**</span></span> <br/> |<span data-ttu-id="fbe1b-127">サウンドを再生できない場合にビープ音を鳴らすかどうかを指定します。ビープ音を鳴らすには、ゼロ以外の数値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="fbe1b-128">_同期_</span><span class="sxs-lookup"><span data-stu-id="fbe1b-128">_synch_</span></span> <br/> |<span data-ttu-id="fbe1b-129">必須</span><span class="sxs-lookup"><span data-stu-id="fbe1b-129">Required</span></span>  <br/> |<span data-ttu-id="fbe1b-130">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="fbe1b-130">**Boolean**</span></span> <br/> |<span data-ttu-id="fbe1b-131">非同期 (0) または同期 (1) のどちらでサウンドを再生するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbe1b-132">注釈</span><span class="sxs-lookup"><span data-stu-id="fbe1b-132">Remarks</span></span>

<span data-ttu-id="fbe1b-133">Visio がサウンドを再生して処理を続行することができますようにサウンドを非同期的に再生する必要があります通常。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="fbe1b-134">いくつかのサウンドは、同期的に、その再生、または一部を再生できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fbe1b-135">例 1</span><span class="sxs-lookup"><span data-stu-id="fbe1b-135">Example 1</span></span>

<span data-ttu-id="fbe1b-136">PLAYSOUND("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="fbe1b-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="fbe1b-137">ウェーブ オーディオ ファイル chord.wav を非同期で実行し、警告のビープ音を鳴らしません。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fbe1b-138">例 2</span><span class="sxs-lookup"><span data-stu-id="fbe1b-138">Example 2</span></span>

<span data-ttu-id="fbe1b-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="fbe1b-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="fbe1b-140">システムのメッセージ (警告) サウンドを非同期で実行し、警告のビープ音を鳴らしません。</span><span class="sxs-lookup"><span data-stu-id="fbe1b-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

