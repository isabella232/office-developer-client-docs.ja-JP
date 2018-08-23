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
description: 番号から Unicode 文字を返します。
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806727"
---
# <a name="unichar-function"></a><span data-ttu-id="430a2-103">UNICHAR 関数</span><span class="sxs-lookup"><span data-stu-id="430a2-103">UNICHAR Function</span></span>

<span data-ttu-id="430a2-104">番号から Unicode 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="430a2-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="430a2-105">構文</span><span class="sxs-lookup"><span data-stu-id="430a2-105">Syntax</span></span>

<span data-ttu-id="430a2-106">UNICHAR (* **番号** *)</span><span class="sxs-lookup"><span data-stu-id="430a2-106">UNICHAR (** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="430a2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="430a2-107">Parameters</span></span>

|<span data-ttu-id="430a2-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="430a2-108">**Name**</span></span>|<span data-ttu-id="430a2-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="430a2-109">**Required/Optional**</span></span>|<span data-ttu-id="430a2-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="430a2-110">**Data Type**</span></span>|<span data-ttu-id="430a2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="430a2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="430a2-112">_number_</span><span class="sxs-lookup"><span data-stu-id="430a2-112">_number_</span></span> <br/> |<span data-ttu-id="430a2-113">必須</span><span class="sxs-lookup"><span data-stu-id="430a2-113">Required</span></span>  <br/> |<span data-ttu-id="430a2-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="430a2-114">**Integer**</span></span> <br/> |<span data-ttu-id="430a2-115">1 ～ 65,535 の整数を指定します。これ以外の数値を指定すると、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="430a2-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="430a2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="430a2-116">Remarks</span></span>

<span data-ttu-id="430a2-117">返される文字列の長さは、Unicode 1 文字の長さ (通常の半角 2 文字分) です。</span><span class="sxs-lookup"><span data-stu-id="430a2-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="430a2-118">例</span><span class="sxs-lookup"><span data-stu-id="430a2-118">Example</span></span>

<span data-ttu-id="430a2-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="430a2-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="430a2-120">(ラテン大文字 A) を返します。</span><span class="sxs-lookup"><span data-stu-id="430a2-120">Returns A (Latin Capital Letter A)</span></span> 
  

