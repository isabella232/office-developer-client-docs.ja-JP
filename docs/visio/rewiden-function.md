---
title: REWIDEN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: 指定した文字セットを使用して、拡張されたシングルバイトまたはマルチバイト文字セットコードの16ビット文字コードを生成する数式を、16ビットの Unicode 文字コードの文字列に変換します。
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326769"
---
# <a name="rewiden-function"></a><span data-ttu-id="cc410-103">REWIDEN 関数</span><span class="sxs-lookup"><span data-stu-id="cc410-103">REWIDEN Function</span></span>

<span data-ttu-id="cc410-104">指定した文字セットを使用して、拡張されたシングルバイトまたはマルチバイト文字セットコードの16ビット文字コードを生成する数式を、16ビットの Unicode 文字コードの文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="cc410-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cc410-105">構文</span><span class="sxs-lookup"><span data-stu-id="cc410-105">Syntax</span></span>

<span data-ttu-id="cc410-106">再拡大 (\* \* *srccharset* \* *、* \* *dstcharset* \* *、* \* *text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="cc410-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cc410-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc410-107">Parameters</span></span>

|<span data-ttu-id="cc410-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="cc410-108">**Name**</span></span>|<span data-ttu-id="cc410-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="cc410-109">**Required/Optional**</span></span>|<span data-ttu-id="cc410-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="cc410-110">**Data Type**</span></span>|<span data-ttu-id="cc410-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="cc410-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cc410-112">_srccharset_</span><span class="sxs-lookup"><span data-stu-id="cc410-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="cc410-113">必須</span><span class="sxs-lookup"><span data-stu-id="cc410-113">Required</span></span>  <br/> |<span data-ttu-id="cc410-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cc410-114">**String**</span></span> <br/> |<span data-ttu-id="cc410-115">変換前の図面の文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="cc410-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="cc410-116">_dstcharset_</span><span class="sxs-lookup"><span data-stu-id="cc410-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="cc410-117">必須</span><span class="sxs-lookup"><span data-stu-id="cc410-117">Required</span></span>  <br/> |<span data-ttu-id="cc410-118">**String**</span><span class="sxs-lookup"><span data-stu-id="cc410-118">**String**</span></span> <br/> | <span data-ttu-id="cc410-119">変換後の図面の文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="cc410-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="cc410-120">_text_</span><span class="sxs-lookup"><span data-stu-id="cc410-120">_text_</span></span> <br/> |<span data-ttu-id="cc410-121">必須</span><span class="sxs-lookup"><span data-stu-id="cc410-121">Required</span></span>  <br/> |<span data-ttu-id="cc410-122">**String**</span><span class="sxs-lookup"><span data-stu-id="cc410-122">**String**</span></span> <br/> |<span data-ttu-id="cc410-123">変換するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="cc410-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc410-124">解説</span><span class="sxs-lookup"><span data-stu-id="cc410-124">Remarks</span></span>

<span data-ttu-id="cc410-p101">REWIDEN 関数は、Visio 2002 の図面から Visio 2003 の図面への自動変換に使用されます。それ以外の使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="cc410-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

