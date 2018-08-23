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
description: 指定した文字セットを使用して、16 ビット Unicode 文字コードの文字列に拡張されたシングル バイトまたはマルチバイト文字セット コードは、16 ビットの文字コードを生成する数式に変換します。
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806239"
---
# <a name="rewiden-function"></a><span data-ttu-id="6b2d7-103">REWIDEN 関数</span><span class="sxs-lookup"><span data-stu-id="6b2d7-103">REWIDEN Function</span></span>

<span data-ttu-id="6b2d7-104">指定した文字セットを使用して、16 ビット Unicode 文字コードの文字列に拡張されたシングル バイトまたはマルチバイト文字セット コードは、16 ビットの文字コードを生成する数式に変換します。</span><span class="sxs-lookup"><span data-stu-id="6b2d7-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6b2d7-105">構文</span><span class="sxs-lookup"><span data-stu-id="6b2d7-105">Syntax</span></span>

<span data-ttu-id="6b2d7-106">REWIDEN (* * *srcCharSet* * *、* * *dstCharSet* * *、* **テキスト** *)</span><span class="sxs-lookup"><span data-stu-id="6b2d7-106">REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6b2d7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b2d7-107">Parameters</span></span>

|<span data-ttu-id="6b2d7-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-108">**Name**</span></span>|<span data-ttu-id="6b2d7-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-109">**Required/Optional**</span></span>|<span data-ttu-id="6b2d7-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-110">**Data Type**</span></span>|<span data-ttu-id="6b2d7-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6b2d7-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="6b2d7-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="6b2d7-113">必須</span><span class="sxs-lookup"><span data-stu-id="6b2d7-113">Required</span></span>  <br/> |<span data-ttu-id="6b2d7-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-114">**String**</span></span> <br/> |<span data-ttu-id="6b2d7-115">変換前の図面の文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b2d7-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="6b2d7-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="6b2d7-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="6b2d7-117">必須</span><span class="sxs-lookup"><span data-stu-id="6b2d7-117">Required</span></span>  <br/> |<span data-ttu-id="6b2d7-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-118">**String**</span></span> <br/> | <span data-ttu-id="6b2d7-119">変換後の図面の文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b2d7-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="6b2d7-120">_text_</span><span class="sxs-lookup"><span data-stu-id="6b2d7-120">_text_</span></span> <br/> |<span data-ttu-id="6b2d7-121">必須</span><span class="sxs-lookup"><span data-stu-id="6b2d7-121">Required</span></span>  <br/> |<span data-ttu-id="6b2d7-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6b2d7-122">**String**</span></span> <br/> |<span data-ttu-id="6b2d7-123">変換するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b2d7-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b2d7-124">注釈</span><span class="sxs-lookup"><span data-stu-id="6b2d7-124">Remarks</span></span>

<span data-ttu-id="6b2d7-p101">REWIDEN 関数は、Visio 2002 の図面から Visio 2003 の図面への自動変換に使用されます。それ以外の使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6b2d7-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

