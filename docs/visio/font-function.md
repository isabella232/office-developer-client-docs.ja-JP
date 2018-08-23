---
title: FONT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: 名前で指定されたフォントの一意識別子の整数値を返します。
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805427"
---
# <a name="font-function"></a><span data-ttu-id="224bb-103">FONT 関数</span><span class="sxs-lookup"><span data-stu-id="224bb-103">FONT Function</span></span>

<span data-ttu-id="224bb-104">名前で指定されたフォントの一意識別子の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="224bb-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="224bb-105">ほとんどの場合は、フォントの識別子は、システム固有です。</span><span class="sxs-lookup"><span data-stu-id="224bb-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="224bb-106">フォントは、ファイルで使用して 1 回確立されたままが**フォント**関数は、システムおよび Visio のバージョン間で特定のフォントを一貫したアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="224bb-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="224bb-107">フォントの識別子への参照を直接ではなくフォントを割り当てるには、**フォント**機能を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="224bb-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="224bb-108">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="224bb-108">Version Information</span></span>

<span data-ttu-id="224bb-109">追加バージョン: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="224bb-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="224bb-110">構文</span><span class="sxs-lookup"><span data-stu-id="224bb-110">Syntax</span></span>

 <span data-ttu-id="224bb-111">**フォント**( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="224bb-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="224bb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="224bb-112">Parameters</span></span>

|<span data-ttu-id="224bb-113">**名前**</span><span class="sxs-lookup"><span data-stu-id="224bb-113">**Name**</span></span>|<span data-ttu-id="224bb-114">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="224bb-114">**Required/Optional**</span></span>|<span data-ttu-id="224bb-115">**データ型**</span><span class="sxs-lookup"><span data-stu-id="224bb-115">**Data Type**</span></span>|<span data-ttu-id="224bb-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="224bb-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="224bb-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="224bb-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="224bb-118">必須</span><span class="sxs-lookup"><span data-stu-id="224bb-118">Required</span></span>  <br/> |<span data-ttu-id="224bb-119">**string**</span><span class="sxs-lookup"><span data-stu-id="224bb-119">**string**</span></span> <br/> |<span data-ttu-id="224bb-120">フォント名を指定します。</span><span class="sxs-lookup"><span data-stu-id="224bb-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="224bb-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="224bb-121">Return value</span></span>

<span data-ttu-id="224bb-122">整数</span><span class="sxs-lookup"><span data-stu-id="224bb-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="224bb-123">注釈</span><span class="sxs-lookup"><span data-stu-id="224bb-123">Remarks</span></span>

<span data-ttu-id="224bb-124">*Font_name_string*の指定された文字列で、フォントが一致しない場合、この関数は、#VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="224bb-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="224bb-125">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="224bb-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="224bb-126">例</span><span class="sxs-lookup"><span data-stu-id="224bb-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="224bb-127">「Calibri」フォントには、一意 ID を表す整数値 (4) を返します。</span><span class="sxs-lookup"><span data-stu-id="224bb-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

