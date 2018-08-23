---
title: EVALTEXT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: および結果を返す数式をされたかのようになります内のテキストを評価します。
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805327"
---
# <a name="evaltext-function"></a><span data-ttu-id="9166c-103">EVALTEXT 関数</span><span class="sxs-lookup"><span data-stu-id="9166c-103">EVALTEXT Function</span></span>

<span data-ttu-id="9166c-104">および結果を返す数式をされたかのように_なります_内のテキストを評価します。</span><span class="sxs-lookup"><span data-stu-id="9166c-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9166c-105">構文</span><span class="sxs-lookup"><span data-stu-id="9166c-105">Syntax</span></span>

<span data-ttu-id="9166c-106">EVALTEXT (* **なります! テキスト** *)</span><span class="sxs-lookup"><span data-stu-id="9166c-106">EVALTEXT(** *shapename!theText* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9166c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9166c-107">Parameters</span></span>

|<span data-ttu-id="9166c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="9166c-108">**Name**</span></span>|<span data-ttu-id="9166c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9166c-109">**Required/Optional**</span></span>|<span data-ttu-id="9166c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9166c-110">**Data Type**</span></span>|<span data-ttu-id="9166c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9166c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9166c-112">_なります! テキスト_</span><span class="sxs-lookup"><span data-stu-id="9166c-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="9166c-113">必須</span><span class="sxs-lookup"><span data-stu-id="9166c-113">Required</span></span>  <br/> |<span data-ttu-id="9166c-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="9166c-114">**String**</span></span> <br/> |<span data-ttu-id="9166c-115">関連付けられている図形のテキスト構成が変更されたときにトリガーされるセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9166c-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9166c-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="9166c-116">Return value</span></span>

<span data-ttu-id="9166c-117">String</span><span class="sxs-lookup"><span data-stu-id="9166c-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9166c-118">注釈</span><span class="sxs-lookup"><span data-stu-id="9166c-118">Remarks</span></span>

 <span data-ttu-id="9166c-119">_shapename_ を使用して、現在の図形以外の図形のテキストを参照できます。</span><span class="sxs-lookup"><span data-stu-id="9166c-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="9166c-p101">テキストがない場合、結果はゼロになります。テキストを評価できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="9166c-p101">If there is no text, the result is zero. If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="9166c-122">例</span><span class="sxs-lookup"><span data-stu-id="9166c-122">Example</span></span>

<span data-ttu-id="9166c-123">EVALTEXT(Line.2!theText)</span><span class="sxs-lookup"><span data-stu-id="9166c-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="9166c-p102">[線 2] 図形に含まれているテキストを評価します。たとえば、[線 2] に "4 ft + 0.5 ft" が含まれている場合、値 4.5 ft を返します。</span><span class="sxs-lookup"><span data-stu-id="9166c-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

