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
description: 引数 offename のテキストを数式として評価し、結果を返します。
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329051"
---
# <a name="evaltext-function"></a><span data-ttu-id="03808-103">EVALTEXT 関数</span><span class="sxs-lookup"><span data-stu-id="03808-103">EVALTEXT Function</span></span>

<span data-ttu-id="03808-104">引数 offename の__ テキストを数式として評価し、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="03808-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="03808-105">構文</span><span class="sxs-lookup"><span data-stu-id="03808-105">Syntax</span></span>

<span data-ttu-id="03808-106">evaltext (\* \* *offename!* text \* \*)</span><span class="sxs-lookup"><span data-stu-id="03808-106">EVALTEXT(\*\* *shapename!theText* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="03808-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="03808-107">Parameters</span></span>

|<span data-ttu-id="03808-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="03808-108">**Name**</span></span>|<span data-ttu-id="03808-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="03808-109">**Required/Optional**</span></span>|<span data-ttu-id="03808-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="03808-110">**Data Type**</span></span>|<span data-ttu-id="03808-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="03808-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="03808-112">_offename! テキスト_</span><span class="sxs-lookup"><span data-stu-id="03808-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="03808-113">必須</span><span class="sxs-lookup"><span data-stu-id="03808-113">Required</span></span>  <br/> |<span data-ttu-id="03808-114">**String**</span><span class="sxs-lookup"><span data-stu-id="03808-114">**String**</span></span> <br/> |<span data-ttu-id="03808-115">関連付けられている図形のテキスト構成が変更されたときにトリガーされるセルを指定します。</span><span class="sxs-lookup"><span data-stu-id="03808-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="03808-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="03808-116">Return value</span></span>

<span data-ttu-id="03808-117">文字列</span><span class="sxs-lookup"><span data-stu-id="03808-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03808-118">注釈</span><span class="sxs-lookup"><span data-stu-id="03808-118">Remarks</span></span>

 <span data-ttu-id="03808-119">_shapename_ を使用して、現在の図形以外の図形のテキストを参照できます。</span><span class="sxs-lookup"><span data-stu-id="03808-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="03808-120">テキストがない場合、結果はゼロになります。</span><span class="sxs-lookup"><span data-stu-id="03808-120">If there is no text, the result is zero.</span></span> <span data-ttu-id="03808-121">テキストを評価できない場合、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="03808-121">If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="03808-122">例</span><span class="sxs-lookup"><span data-stu-id="03808-122">Example</span></span>

<span data-ttu-id="03808-123">evaltext (Line. 2! テキスト)</span><span class="sxs-lookup"><span data-stu-id="03808-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="03808-p102">[線 2] 図形に含まれているテキストを評価します。たとえば、[線 2] に "4 ft + 0.5 ft" が含まれている場合、値 4.5 ft を返します。</span><span class="sxs-lookup"><span data-stu-id="03808-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

