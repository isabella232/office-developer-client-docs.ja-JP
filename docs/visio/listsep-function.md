---
title: LISTSEP 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
localization_priority: Normal
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: 現在のユーザーロケールのリスト区切り文字列を返します。
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322345"
---
# <a name="listsep-function"></a><span data-ttu-id="08ed7-103">LISTSEP 関数</span><span class="sxs-lookup"><span data-stu-id="08ed7-103">LISTSEP Function</span></span>

<span data-ttu-id="08ed7-104">現在のユーザーロケールのリスト区切り文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="08ed7-104">Returns the list-separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="08ed7-105">構文</span><span class="sxs-lookup"><span data-stu-id="08ed7-105">Syntax</span></span>

<span data-ttu-id="08ed7-106">LISTSEP ()</span><span class="sxs-lookup"><span data-stu-id="08ed7-106">LISTSEP ()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="08ed7-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="08ed7-107">Return value</span></span>

<span data-ttu-id="08ed7-108">String</span><span class="sxs-lookup"><span data-stu-id="08ed7-108">String</span></span>
  
## <a name="example"></a><span data-ttu-id="08ed7-109">例</span><span class="sxs-lookup"><span data-stu-id="08ed7-109">Example</span></span>

<span data-ttu-id="08ed7-110">setf (getref (ユーザーエクステント), "MAX (Width" &amp; listsep () &amp; "Height)")</span><span class="sxs-lookup"><span data-stu-id="08ed7-110">SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)")</span></span> 
  

