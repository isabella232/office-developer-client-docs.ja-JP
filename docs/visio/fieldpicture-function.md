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
description: Microsoft Visio の内部テキストフィールドの書式設定コードと一致する形式の画像文字列を返します。
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322548"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="c7edb-103">FIELDPICTURE 関数</span><span class="sxs-lookup"><span data-stu-id="c7edb-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="c7edb-104">Microsoft Visio の内部テキストフィールドの書式設定コードと一致する形式の画像文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="c7edb-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c7edb-105">構文</span><span class="sxs-lookup"><span data-stu-id="c7edb-105">Syntax</span></span>

<span data-ttu-id="c7edb-106">fieldpicture (\* \* *code* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c7edb-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c7edb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c7edb-107">Parameters</span></span>

|<span data-ttu-id="c7edb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c7edb-108">**Name**</span></span>|<span data-ttu-id="c7edb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c7edb-109">**Required/Optional**</span></span>|<span data-ttu-id="c7edb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c7edb-110">**Data Type**</span></span>|<span data-ttu-id="c7edb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c7edb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c7edb-112">_code_</span><span class="sxs-lookup"><span data-stu-id="c7edb-112">_code_</span></span> <br/> |<span data-ttu-id="c7edb-113">必須</span><span class="sxs-lookup"><span data-stu-id="c7edb-113">Required</span></span>  <br/> |<span data-ttu-id="c7edb-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="c7edb-114">**Number**</span></span> <br/> | <span data-ttu-id="c7edb-115">テキスト フィールドの書式設定コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="c7edb-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c7edb-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="c7edb-116">Return value</span></span>

<span data-ttu-id="c7edb-117">文字列</span><span class="sxs-lookup"><span data-stu-id="c7edb-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7edb-118">注釈</span><span class="sxs-lookup"><span data-stu-id="c7edb-118">Remarks</span></span>

<span data-ttu-id="c7edb-119">日付、時刻、数値、および単位ラベルに対応した値を定義するには、FORMAT 関数で書式形式の文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7edb-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="c7edb-120">例</span><span class="sxs-lookup"><span data-stu-id="c7edb-120">Example</span></span>

<span data-ttu-id="c7edb-121">fieldpicture (0)</span><span class="sxs-lookup"><span data-stu-id="c7edb-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="c7edb-122">書式形式の文字列 "esc(0)" を返します。この文字列を FORMAT 関数で使用する場合、小数点以下 1 位までと小文字の単位を含む数値を指定することになります。</span><span class="sxs-lookup"><span data-stu-id="c7edb-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

