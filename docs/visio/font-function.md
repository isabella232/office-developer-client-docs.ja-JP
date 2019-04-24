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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346138"
---
# <a name="font-function"></a><span data-ttu-id="9d253-103">FONT 関数</span><span class="sxs-lookup"><span data-stu-id="9d253-103">FONT Function</span></span>

<span data-ttu-id="9d253-104">名前で指定されたフォントの一意識別子の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="9d253-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9d253-105">ほとんどの場合、フォント識別子はシステム固有です。</span><span class="sxs-lookup"><span data-stu-id="9d253-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="9d253-106">フォントはファイル内で使用された後も確立されたままですが、**フォント**関数を使用すると、Visio のシステムおよびバージョン間で特定のフォントに一貫したアクセスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="9d253-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="9d253-107">フォント識別子を直接参照するのではなく、**FONT** 関数を使用してフォントを割り当てることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9d253-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="9d253-108">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="9d253-108">Version Information</span></span>

<span data-ttu-id="9d253-109">追加バージョン: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="9d253-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9d253-110">構文</span><span class="sxs-lookup"><span data-stu-id="9d253-110">Syntax</span></span>

 <span data-ttu-id="9d253-111">**フォント**( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="9d253-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="9d253-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9d253-112">Parameters</span></span>

|<span data-ttu-id="9d253-113">**名前**</span><span class="sxs-lookup"><span data-stu-id="9d253-113">**Name**</span></span>|<span data-ttu-id="9d253-114">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9d253-114">**Required/Optional**</span></span>|<span data-ttu-id="9d253-115">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9d253-115">**Data Type**</span></span>|<span data-ttu-id="9d253-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="9d253-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9d253-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="9d253-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="9d253-118">必須</span><span class="sxs-lookup"><span data-stu-id="9d253-118">Required</span></span>  <br/> |<span data-ttu-id="9d253-119">**string**</span><span class="sxs-lookup"><span data-stu-id="9d253-119">**string**</span></span> <br/> |<span data-ttu-id="9d253-120">フォントの名前。</span><span class="sxs-lookup"><span data-stu-id="9d253-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="9d253-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="9d253-121">Return value</span></span>

<span data-ttu-id="9d253-122">整数</span><span class="sxs-lookup"><span data-stu-id="9d253-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d253-123">解説</span><span class="sxs-lookup"><span data-stu-id="9d253-123">Remarks</span></span>

<span data-ttu-id="9d253-124">*font_name_string*に指定された文字列が既知のフォントと一致しない場合、この関数は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="9d253-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="9d253-125">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="9d253-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9d253-126">例</span><span class="sxs-lookup"><span data-stu-id="9d253-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="9d253-127">"Calibri" フォントの一意の ID を表す整数値 (4) を返します。</span><span class="sxs-lookup"><span data-stu-id="9d253-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

