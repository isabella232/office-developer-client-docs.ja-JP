---
title: FONT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: 名前で指定されたフォントの一意識別子の整数値を返します。
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422174"
---
# <a name="font-function"></a><span data-ttu-id="412cc-103">FONT 関数</span><span class="sxs-lookup"><span data-stu-id="412cc-103">FONT Function</span></span>

<span data-ttu-id="412cc-104">名前で指定されたフォントの一意識別子の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="412cc-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="412cc-105">ほとんどの場合、フォント識別子はシステム固有です。</span><span class="sxs-lookup"><span data-stu-id="412cc-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="412cc-106">フォントはファイルで一度使われると確立されたままですが **、FONT** 関数はシステムやバージョンのフォント間で特定のフォントに一貫したアクセスVisio。</span><span class="sxs-lookup"><span data-stu-id="412cc-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="412cc-107">フォント識別子を直接参照するのではなく、**FONT** 関数を使用してフォントを割り当てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="412cc-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="412cc-108">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="412cc-108">Version Information</span></span>

<span data-ttu-id="412cc-109">追加バージョン: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="412cc-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="412cc-110">構文</span><span class="sxs-lookup"><span data-stu-id="412cc-110">Syntax</span></span>

 <span data-ttu-id="412cc-111">**FONT**( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="412cc-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="412cc-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="412cc-112">Parameters</span></span>

|<span data-ttu-id="412cc-113">**名前**</span><span class="sxs-lookup"><span data-stu-id="412cc-113">**Name**</span></span>|<span data-ttu-id="412cc-114">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="412cc-114">**Required/Optional**</span></span>|<span data-ttu-id="412cc-115">**データ型**</span><span class="sxs-lookup"><span data-stu-id="412cc-115">**Data Type**</span></span>|<span data-ttu-id="412cc-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="412cc-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="412cc-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="412cc-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="412cc-118">必須</span><span class="sxs-lookup"><span data-stu-id="412cc-118">Required</span></span>  <br/> |<span data-ttu-id="412cc-119">**string**</span><span class="sxs-lookup"><span data-stu-id="412cc-119">**string**</span></span> <br/> |<span data-ttu-id="412cc-120">フォントの名前。</span><span class="sxs-lookup"><span data-stu-id="412cc-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="412cc-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="412cc-121">Return value</span></span>

<span data-ttu-id="412cc-122">整数</span><span class="sxs-lookup"><span data-stu-id="412cc-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="412cc-123">注釈</span><span class="sxs-lookup"><span data-stu-id="412cc-123">Remarks</span></span>

<span data-ttu-id="412cc-124">指定した文字列が既知の  *フォントfont_name_string*  一致しない場合、この関数は既知のフォントを#VALUE!</span><span class="sxs-lookup"><span data-stu-id="412cc-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="412cc-125">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="412cc-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="412cc-126">例</span><span class="sxs-lookup"><span data-stu-id="412cc-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="412cc-127">"Calibri" フォントの一意の ID を表す整数値 (4) を返します。</span><span class="sxs-lookup"><span data-stu-id="412cc-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

