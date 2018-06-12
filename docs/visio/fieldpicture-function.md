---
title: FIELDPICTURE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Microsoft Visio の内部のテキスト フィールドの表示形式コードに一致する図の書式設定文字列を返します。
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805351"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="5afd5-103">FIELDPICTURE 関数</span><span class="sxs-lookup"><span data-stu-id="5afd5-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="5afd5-104">Microsoft Visio の内部のテキスト フィールドの表示形式コードに一致する図の書式設定文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5afd5-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5afd5-105">構文</span><span class="sxs-lookup"><span data-stu-id="5afd5-105">Syntax</span></span>

<span data-ttu-id="5afd5-106">FIELDPICTURE (* **コード** *)</span><span class="sxs-lookup"><span data-stu-id="5afd5-106">FIELDPICTURE(** *code* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5afd5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5afd5-107">Parameters</span></span>

|<span data-ttu-id="5afd5-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5afd5-108">**Name**</span></span>|<span data-ttu-id="5afd5-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5afd5-109">**Required/Optional**</span></span>|<span data-ttu-id="5afd5-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5afd5-110">**Data Type**</span></span>|<span data-ttu-id="5afd5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5afd5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5afd5-112">_code_</span><span class="sxs-lookup"><span data-stu-id="5afd5-112">_code_</span></span> <br/> |<span data-ttu-id="5afd5-113">必須</span><span class="sxs-lookup"><span data-stu-id="5afd5-113">Required</span></span>  <br/> |<span data-ttu-id="5afd5-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="5afd5-114">**Number**</span></span> <br/> | <span data-ttu-id="5afd5-115">テキスト フィールドの書式設定コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="5afd5-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5afd5-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5afd5-116">Return value</span></span>

<span data-ttu-id="5afd5-117">文字列</span><span class="sxs-lookup"><span data-stu-id="5afd5-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5afd5-118">注釈</span><span class="sxs-lookup"><span data-stu-id="5afd5-118">Remarks</span></span>

<span data-ttu-id="5afd5-119">日付、時刻、数値、および単位ラベルに対応した値を定義するには、FORMAT 関数で書式形式の文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="5afd5-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="5afd5-120">例</span><span class="sxs-lookup"><span data-stu-id="5afd5-120">Example</span></span>

<span data-ttu-id="5afd5-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="5afd5-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="5afd5-122">書式形式の文字列 "esc(0)" を返します。この文字列を FORMAT 関数で使用する場合、小数点以下 1 位までと小文字の単位を含む数値を指定することになります。</span><span class="sxs-lookup"><span data-stu-id="5afd5-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

