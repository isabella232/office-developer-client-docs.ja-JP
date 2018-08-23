---
title: LISTSHEETREF 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: 図形を含む、指定されたリスト コンテナー図形のシート参照を返します。
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805750"
---
# <a name="listsheetref-function"></a><span data-ttu-id="f6e9e-103">LISTSHEETREF 関数</span><span class="sxs-lookup"><span data-stu-id="f6e9e-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="f6e9e-104">図形を含む、指定されたリスト コンテナー図形のシート参照を返します。</span><span class="sxs-lookup"><span data-stu-id="f6e9e-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="f6e9e-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="f6e9e-105">Version Information</span></span>

<span data-ttu-id="f6e9e-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="f6e9e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f6e9e-107">構文</span><span class="sxs-lookup"><span data-stu-id="f6e9e-107">Syntax</span></span>

<span data-ttu-id="f6e9e-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="f6e9e-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="f6e9e-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="f6e9e-109">Return value</span></span>

<span data-ttu-id="f6e9e-110">シェイプシート参照</span><span class="sxs-lookup"><span data-stu-id="f6e9e-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6e9e-111">注釈</span><span class="sxs-lookup"><span data-stu-id="f6e9e-111">Remarks</span></span>

<span data-ttu-id="f6e9e-112">図形がリスト メンバーではない場合、LISTSHEETREF 関数は #REF! を返します。</span><span class="sxs-lookup"><span data-stu-id="f6e9e-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="f6e9e-113">例</span><span class="sxs-lookup"><span data-stu-id="f6e9e-113">Example</span></span>

<span data-ttu-id="f6e9e-114">LISTSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="f6e9e-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="f6e9e-115">図形を含むリスト コンテナー図形の [Height] セルの値を返します。</span><span class="sxs-lookup"><span data-stu-id="f6e9e-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

