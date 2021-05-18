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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423014"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="15269-103">CALLOUTTARGETREF 関数</span><span class="sxs-lookup"><span data-stu-id="15269-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="15269-104">引き出し図形の対象図形のシート参照を返します。</span><span class="sxs-lookup"><span data-stu-id="15269-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="15269-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="15269-105">Version Information</span></span>

<span data-ttu-id="15269-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="15269-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="15269-107">構文</span><span class="sxs-lookup"><span data-stu-id="15269-107">Syntax</span></span>

<span data-ttu-id="15269-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="15269-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="15269-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="15269-109">Return value</span></span>

<span data-ttu-id="15269-110">シェイプシート参照</span><span class="sxs-lookup"><span data-stu-id="15269-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15269-111">注釈</span><span class="sxs-lookup"><span data-stu-id="15269-111">Remarks</span></span>

<span data-ttu-id="15269-112">図形が引き出し図形ではない場合、またはターゲット図形に関連付けされていない場合、CALLOUTTARGETREF は次の#REF。</span><span class="sxs-lookup"><span data-stu-id="15269-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="15269-113">例</span><span class="sxs-lookup"><span data-stu-id="15269-113">Example</span></span>

<span data-ttu-id="15269-114">CALLOUTTARGETREF()!Height</span><span class="sxs-lookup"><span data-stu-id="15269-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="15269-115">引き出しに関連付けられた図形の [Height] セルの値を返します。</span><span class="sxs-lookup"><span data-stu-id="15269-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

