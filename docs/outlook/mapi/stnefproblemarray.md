---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336499"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="0eb1e-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="0eb1e-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="0eb1e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eb1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eb1e-105">トランスポートニュートラルカプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生した1つ以上の処理上の問題について説明する**STnefProblem**構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0eb1e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0eb1e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0eb1e-107">Tnef</span><span class="sxs-lookup"><span data-stu-id="0eb1e-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="0eb1e-108">Members</span><span class="sxs-lookup"><span data-stu-id="0eb1e-108">Members</span></span>

 <span data-ttu-id="0eb1e-109">**cproblem**</span><span class="sxs-lookup"><span data-stu-id="0eb1e-109">**cProblem**</span></span>
  
> <span data-ttu-id="0eb1e-110">**aproblem**メンバーで指定されている配列内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="0eb1e-111">**aproblem**</span><span class="sxs-lookup"><span data-stu-id="0eb1e-111">**aProblem**</span></span>
  
> <span data-ttu-id="0eb1e-112">[STnefProblem](stnefproblem.md)構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="0eb1e-113">各構造体には、プロパティまたは属性処理の問題に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0eb1e-114">解説</span><span class="sxs-lookup"><span data-stu-id="0eb1e-114">Remarks</span></span>

<span data-ttu-id="0eb1e-115">属性またはプロパティの処理中に問題が発生した場合、 [ITnef:: ExtractProps](itnef-extractprops.md)メソッドと[ITnef:: Finish](itnef-finish.md)メソッドの出力パラメーターは、それぞれ**STnefProblemArray**構造体へのポインターを受け取り、 **ExtractProps\*\*\*\*完了**するたびに、MAPI_W_ERRORS_RETURNED 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="0eb1e-116">このエラー値は、処理中に問題が発生し、 **STnefProblemArray**構造が生成されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="0eb1e-117">属性またはプロパティの処理中に**STnefProblem**構造体が生成されない場合、クライアントアプリケーションは、その属性またはプロパティの処理が正常に終了したことを前提として続行できます。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="0eb1e-118">唯一の例外は、カプセル化ブロックのデコード中に問題が発生した場合です。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="0eb1e-119">このデコード中にエラーが発生した場合は、MAPI_E_UNABLE_TO_COMPLETE を構造内の[SCODE](scode.md)として返すことができます。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="0eb1e-120">この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが続行されます。</span><span class="sxs-lookup"><span data-stu-id="0eb1e-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0eb1e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="0eb1e-121">See also</span></span>



[<span data-ttu-id="0eb1e-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="0eb1e-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="0eb1e-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="0eb1e-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="0eb1e-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0eb1e-124">MAPI Structures</span></span>](mapi-structures.md)

