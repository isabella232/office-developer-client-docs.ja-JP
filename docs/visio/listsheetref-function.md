---
title: LISTSHEETREF 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: 図形を含む、指定されたリスト コンテナー図形のシート参照を返します。
ms.openlocfilehash: 748a248f68345e97e97ca90a4603b6e164a551c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429552"
---
# <a name="listsheetref-function"></a><span data-ttu-id="60d68-103">LISTSHEETREF 関数</span><span class="sxs-lookup"><span data-stu-id="60d68-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="60d68-104">図形を含む、指定されたリスト コンテナー図形のシート参照を返します。</span><span class="sxs-lookup"><span data-stu-id="60d68-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="60d68-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="60d68-105">Version Information</span></span>

<span data-ttu-id="60d68-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="60d68-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="60d68-107">構文</span><span class="sxs-lookup"><span data-stu-id="60d68-107">Syntax</span></span>

<span data-ttu-id="60d68-108">LISTMEMBERCOUNT ()</span><span class="sxs-lookup"><span data-stu-id="60d68-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="60d68-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="60d68-109">Return value</span></span>

<span data-ttu-id="60d68-110">シェイプシート参照</span><span class="sxs-lookup"><span data-stu-id="60d68-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60d68-111">注釈</span><span class="sxs-lookup"><span data-stu-id="60d68-111">Remarks</span></span>

<span data-ttu-id="60d68-112">図形がリスト メンバーではない場合、LISTSHEETREF 関数は #REF! を返します。</span><span class="sxs-lookup"><span data-stu-id="60d68-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="60d68-113">例</span><span class="sxs-lookup"><span data-stu-id="60d68-113">Example</span></span>

<span data-ttu-id="60d68-114">listsheetref (1)!寸法</span><span class="sxs-lookup"><span data-stu-id="60d68-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="60d68-115">図形を含むリスト コンテナー図形の [Height] セルの値を返します。</span><span class="sxs-lookup"><span data-stu-id="60d68-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

