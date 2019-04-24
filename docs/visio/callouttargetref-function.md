---
title: CALLOUTTARGETREF 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: 引き出し図形の対象図形のシート参照を返します。
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337248"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="36e6b-103">CALLOUTTARGETREF 関数</span><span class="sxs-lookup"><span data-stu-id="36e6b-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="36e6b-104">引き出し図形の対象図形のシート参照を返します。</span><span class="sxs-lookup"><span data-stu-id="36e6b-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="36e6b-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="36e6b-105">Version Information</span></span>

<span data-ttu-id="36e6b-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="36e6b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36e6b-107">構文</span><span class="sxs-lookup"><span data-stu-id="36e6b-107">Syntax</span></span>

<span data-ttu-id="36e6b-108">CALLOUTTARGETREF ()!</span><span class="sxs-lookup"><span data-stu-id="36e6b-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="36e6b-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="36e6b-109">Return value</span></span>

<span data-ttu-id="36e6b-110">シェイプシート参照</span><span class="sxs-lookup"><span data-stu-id="36e6b-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36e6b-111">解説</span><span class="sxs-lookup"><span data-stu-id="36e6b-111">Remarks</span></span>

<span data-ttu-id="36e6b-112">図形が引き出し図形ではない場合、または図形が対象の図形に関連付けられていない場合、CALLOUTTARGETREF は #REF を返します。</span><span class="sxs-lookup"><span data-stu-id="36e6b-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="36e6b-113">例</span><span class="sxs-lookup"><span data-stu-id="36e6b-113">Example</span></span>

<span data-ttu-id="36e6b-114">CALLOUTTARGETREF ()!寸法</span><span class="sxs-lookup"><span data-stu-id="36e6b-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="36e6b-115">引き出しに関連付けられた図形の [Height] セルの値を返します。</span><span class="sxs-lookup"><span data-stu-id="36e6b-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

