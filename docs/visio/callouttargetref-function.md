---
title: CALLOUTTARGETREF 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: 引き出し図形の対象図形のシート参照を返します。
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804927"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="316a9-103">CALLOUTTARGETREF 関数</span><span class="sxs-lookup"><span data-stu-id="316a9-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="316a9-104">引き出し図形の対象図形のシート参照を返します。</span><span class="sxs-lookup"><span data-stu-id="316a9-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="316a9-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="316a9-105">Version Information</span></span>

<span data-ttu-id="316a9-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="316a9-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="316a9-107">構文</span><span class="sxs-lookup"><span data-stu-id="316a9-107">Syntax</span></span>

<span data-ttu-id="316a9-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="316a9-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="316a9-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="316a9-109">Return value</span></span>

<span data-ttu-id="316a9-110">シェイプシート参照</span><span class="sxs-lookup"><span data-stu-id="316a9-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="316a9-111">注釈</span><span class="sxs-lookup"><span data-stu-id="316a9-111">Remarks</span></span>

<span data-ttu-id="316a9-112">図形が吹き出し図形でない場合、または接続先の図形に関連付けされていない場合は、CALLOUTTARGETREF は、#REF を返します。</span><span class="sxs-lookup"><span data-stu-id="316a9-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="316a9-113">例</span><span class="sxs-lookup"><span data-stu-id="316a9-113">Example</span></span>

<span data-ttu-id="316a9-114">CALLOUTTARGETREF()!Height</span><span class="sxs-lookup"><span data-stu-id="316a9-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="316a9-115">引き出しに関連付けられた図形の [Height] セルの値を返します。</span><span class="sxs-lookup"><span data-stu-id="316a9-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

