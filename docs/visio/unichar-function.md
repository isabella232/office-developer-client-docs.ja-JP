---
title: UNICHAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: 数値から Unicode 文字を返します。
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417582"
---
# <a name="unichar-function"></a><span data-ttu-id="c9f3b-103">UNICHAR 関数</span><span class="sxs-lookup"><span data-stu-id="c9f3b-103">UNICHAR Function</span></span>

<span data-ttu-id="c9f3b-104">数値から Unicode 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="c9f3b-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c9f3b-105">構文</span><span class="sxs-lookup"><span data-stu-id="c9f3b-105">Syntax</span></span>

<span data-ttu-id="c9f3b-106">ユニケース har (\* \* *number* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c9f3b-106">UNICHAR (\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c9f3b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c9f3b-107">Parameters</span></span>

|<span data-ttu-id="c9f3b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c9f3b-108">**Name**</span></span>|<span data-ttu-id="c9f3b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c9f3b-109">**Required/Optional**</span></span>|<span data-ttu-id="c9f3b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c9f3b-110">**Data Type**</span></span>|<span data-ttu-id="c9f3b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9f3b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c9f3b-112">_number_</span><span class="sxs-lookup"><span data-stu-id="c9f3b-112">_number_</span></span> <br/> |<span data-ttu-id="c9f3b-113">必須</span><span class="sxs-lookup"><span data-stu-id="c9f3b-113">Required</span></span>  <br/> |<span data-ttu-id="c9f3b-114">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="c9f3b-114">**Integer**</span></span> <br/> |<span data-ttu-id="c9f3b-115">1 ～ 65,535 の整数を指定します。これ以外の数値を指定すると、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="c9f3b-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9f3b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c9f3b-116">Remarks</span></span>

<span data-ttu-id="c9f3b-117">返される文字列の長さは、Unicode 1 文字の長さ (通常の半角 2 文字分) です。</span><span class="sxs-lookup"><span data-stu-id="c9f3b-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c9f3b-118">例</span><span class="sxs-lookup"><span data-stu-id="c9f3b-118">Example</span></span>

<span data-ttu-id="c9f3b-119">ユニケース har (65)</span><span class="sxs-lookup"><span data-stu-id="c9f3b-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="c9f3b-120">a (英大文字 a) を返します。</span><span class="sxs-lookup"><span data-stu-id="c9f3b-120">Returns A (Latin Capital Letter A)</span></span> 
  

