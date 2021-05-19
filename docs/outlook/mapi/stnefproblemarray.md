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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434264"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="03c0c-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="03c0c-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="03c0c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03c0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03c0c-105">トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生した 1 つ以上の処理の問題を説明する **STnefProblem** 構造体の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="03c0c-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03c0c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="03c0c-106">Header file:</span></span>  <br/> |<span data-ttu-id="03c0c-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="03c0c-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="03c0c-108">Members</span><span class="sxs-lookup"><span data-stu-id="03c0c-108">Members</span></span>

 <span data-ttu-id="03c0c-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="03c0c-109">**cProblem**</span></span>
  
> <span data-ttu-id="03c0c-110">aProblem メンバーで指定された配列 **内の要素の** 数。</span><span class="sxs-lookup"><span data-stu-id="03c0c-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="03c0c-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="03c0c-111">**aProblem**</span></span>
  
> <span data-ttu-id="03c0c-112">[STnefProblem 構造体の](stnefproblem.md)配列。</span><span class="sxs-lookup"><span data-stu-id="03c0c-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="03c0c-113">各構造には、プロパティまたは属性処理の問題に関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="03c0c-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="03c0c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="03c0c-114">Remarks</span></span>

<span data-ttu-id="03c0c-115">属性またはプロパティの処理中に問題が発生した場合 [、ITnef::ExtractProps](itnef-extractprops.md) メソッドと [ITnef::Finish](itnef-finish.md) メソッドの出力パラメーターは、それぞれ **STnefProblemArray** 構造体へのポインターを受け取り **、ExtractProps** and **Finish** は値 MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="03c0c-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="03c0c-116">このエラー値は、処理中に問題が発生し **、STnefProblemArray 構造が生成されたかどうかを** 示します。</span><span class="sxs-lookup"><span data-stu-id="03c0c-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="03c0c-117">属性またはプロパティの処理中に **STnefProblem** 構造体が生成されない場合、クライアント アプリケーションは、その属性またはプロパティの処理が成功したという前提で続行できます。</span><span class="sxs-lookup"><span data-stu-id="03c0c-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="03c0c-118">カプセル化ブロックのデコード中に問題が発生した場合、唯一の例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="03c0c-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="03c0c-119">このデコード中にエラーが発生した場合、MAPI_E_UNABLE_TO_COMPLETEで [SCODE として](scode.md) 返されます。</span><span class="sxs-lookup"><span data-stu-id="03c0c-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="03c0c-120">この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが継続されます。</span><span class="sxs-lookup"><span data-stu-id="03c0c-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03c0c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="03c0c-121">See also</span></span>



[<span data-ttu-id="03c0c-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="03c0c-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="03c0c-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="03c0c-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="03c0c-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="03c0c-124">MAPI Structures</span></span>](mapi-structures.md)

