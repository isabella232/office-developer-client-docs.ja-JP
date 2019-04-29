---
title: IFERROR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: エラーとして評価されない場合、プライマリ式の評価結果を返します。 エラーの場合は、代替式の評価結果を返します。
ms.openlocfilehash: 7b9b42b5c7e7053bae862ddadf17e65015d8ecc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431177"
---
# <a name="iferror-function"></a><span data-ttu-id="12bcd-104">IFERROR 関数</span><span class="sxs-lookup"><span data-stu-id="12bcd-104">IFERROR Function</span></span>

<span data-ttu-id="12bcd-105">エラーとして評価されない場合、プライマリ式の評価結果を返します。</span><span class="sxs-lookup"><span data-stu-id="12bcd-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="12bcd-106">エラーの場合は、代替式の評価結果を返します。</span><span class="sxs-lookup"><span data-stu-id="12bcd-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="12bcd-107">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="12bcd-107">Version Information</span></span>

<span data-ttu-id="12bcd-108">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="12bcd-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="12bcd-109">構文</span><span class="sxs-lookup"><span data-stu-id="12bcd-109">Syntax</span></span>

<span data-ttu-id="12bcd-110">IFERROR (\* **主式** *、* **代替式** \*)</span><span class="sxs-lookup"><span data-stu-id="12bcd-110">IFERROR(\*\* *primary expression* \*\*, \*\* *alternate expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="12bcd-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="12bcd-111">Parameters</span></span>

|<span data-ttu-id="12bcd-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="12bcd-112">**Name**</span></span>|<span data-ttu-id="12bcd-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="12bcd-113">**Required/Optional**</span></span>|<span data-ttu-id="12bcd-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="12bcd-114">**Data Type**</span></span>|<span data-ttu-id="12bcd-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="12bcd-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="12bcd-116">_プライマリ式_</span><span class="sxs-lookup"><span data-stu-id="12bcd-116">_primary expression_</span></span> <br/> |<span data-ttu-id="12bcd-117">必須</span><span class="sxs-lookup"><span data-stu-id="12bcd-117">Required</span></span>  <br/> |<span data-ttu-id="12bcd-118">**String**</span><span class="sxs-lookup"><span data-stu-id="12bcd-118">**String**</span></span> <br/> |<span data-ttu-id="12bcd-119">評価する最初の式。</span><span class="sxs-lookup"><span data-stu-id="12bcd-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="12bcd-120">_代替式_</span><span class="sxs-lookup"><span data-stu-id="12bcd-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="12bcd-121">必須</span><span class="sxs-lookup"><span data-stu-id="12bcd-121">Required</span></span>  <br/> |<span data-ttu-id="12bcd-122">**String**</span><span class="sxs-lookup"><span data-stu-id="12bcd-122">**String**</span></span> <br/> |<span data-ttu-id="12bcd-123">一次式がエラーに評価される場合に評価する代替式。</span><span class="sxs-lookup"><span data-stu-id="12bcd-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="12bcd-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="12bcd-124">Return value</span></span>

<span data-ttu-id="12bcd-125">さまざま</span><span class="sxs-lookup"><span data-stu-id="12bcd-125">Varies</span></span>
  

