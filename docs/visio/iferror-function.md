---
title: IFERROR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: エラーが発生すると評価されない場合は、1 次の式の評価結果を返します。 それ以外の場合、代替式の評価結果を返します。
ms.openlocfilehash: 5915d0cb8219ced190c6b53043188c96d2b56b5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805570"
---
# <a name="iferror-function"></a><span data-ttu-id="26b36-104">IFERROR 関数</span><span class="sxs-lookup"><span data-stu-id="26b36-104">IFERROR Function</span></span>

<span data-ttu-id="26b36-105">エラーが発生すると評価されない場合は、1 次の式の評価結果を返します。</span><span class="sxs-lookup"><span data-stu-id="26b36-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="26b36-106">それ以外の場合、代替式の評価結果を返します。</span><span class="sxs-lookup"><span data-stu-id="26b36-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="26b36-107">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="26b36-107">Version Information</span></span>

<span data-ttu-id="26b36-108">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="26b36-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="26b36-109">構文</span><span class="sxs-lookup"><span data-stu-id="26b36-109">Syntax</span></span>

<span data-ttu-id="26b36-110">IFERROR (* **式** *、* **代替式** *)</span><span class="sxs-lookup"><span data-stu-id="26b36-110">IFERROR(** *primary expression* **, ** *alternate expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="26b36-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="26b36-111">Parameters</span></span>

|<span data-ttu-id="26b36-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="26b36-112">**Name**</span></span>|<span data-ttu-id="26b36-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="26b36-113">**Required/Optional**</span></span>|<span data-ttu-id="26b36-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="26b36-114">**Data Type**</span></span>|<span data-ttu-id="26b36-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="26b36-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="26b36-116">_プライマリ式_</span><span class="sxs-lookup"><span data-stu-id="26b36-116">_primary expression_</span></span> <br/> |<span data-ttu-id="26b36-117">必須</span><span class="sxs-lookup"><span data-stu-id="26b36-117">Required</span></span>  <br/> |<span data-ttu-id="26b36-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="26b36-118">**String**</span></span> <br/> |<span data-ttu-id="26b36-119">評価する最初の式。</span><span class="sxs-lookup"><span data-stu-id="26b36-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="26b36-120">_代替式_</span><span class="sxs-lookup"><span data-stu-id="26b36-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="26b36-121">必須</span><span class="sxs-lookup"><span data-stu-id="26b36-121">Required</span></span>  <br/> |<span data-ttu-id="26b36-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="26b36-122">**String**</span></span> <br/> |<span data-ttu-id="26b36-123">一次式がエラーに評価される場合に評価する代替式。</span><span class="sxs-lookup"><span data-stu-id="26b36-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="26b36-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="26b36-124">Return value</span></span>

<span data-ttu-id="26b36-125">可変型 (Varies)</span><span class="sxs-lookup"><span data-stu-id="26b36-125">Varies</span></span>
  

