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
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563507"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="61789-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="61789-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="61789-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61789-105">エンコード中に発生した問題を処理する 1 つまたは複数、またはトランスポート ニュートラル カプセル化形式 (TNEF) ストリームのデコードを記述する**STnefProblem**構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61789-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61789-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="61789-106">Header file:</span></span>  <br/> |<span data-ttu-id="61789-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="61789-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="61789-108">Members</span><span class="sxs-lookup"><span data-stu-id="61789-108">Members</span></span>

 <span data-ttu-id="61789-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="61789-109">**cProblem**</span></span>
  
> <span data-ttu-id="61789-110">**かかわる問題**のメンバーで指定された配列内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="61789-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="61789-111">**かかわる問題**</span><span class="sxs-lookup"><span data-stu-id="61789-111">**aProblem**</span></span>
  
> <span data-ttu-id="61789-112">[STnefProblem](stnefproblem.md)構造体の配列です。</span><span class="sxs-lookup"><span data-stu-id="61789-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="61789-113">各構造体には、プロパティまたは属性の問題の処理に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61789-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="61789-114">注釈</span><span class="sxs-lookup"><span data-stu-id="61789-114">Remarks</span></span>

<span data-ttu-id="61789-115">[ITnef::ExtractProps](itnef-extractprops.md)メソッドと[ITnef::Finish](itnef-finish.md)メソッドの出力パラメーターが、構造体の**STnefProblemArray**と**ExtractProps へのポインターを受信する属性またはプロパティの処理中に問題が発生した場合****終了**各 MAPI_W_ERRORS_RETURNED の値を返すとします。</span><span class="sxs-lookup"><span data-stu-id="61789-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="61789-116">このエラー値は、処理中に問題が発生したし、 **STnefProblemArray**構造体が生成されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="61789-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="61789-117">**STnefProblem**構造体は、属性またはプロパティの処理中に生成されていない場合場合は、クライアント アプリケーションがその属性またはプロパティの処理が成功したことがあると仮定して続行できます。</span><span class="sxs-lookup"><span data-stu-id="61789-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="61789-118">唯一の例外は、ブロックをカプセル化のデコード中に問題が発生したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="61789-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="61789-119">このデコード中にエラーが発生した場合は、構造体に[SCODE](scode.md)として MAPI_E_UNABLE_TO_COMPLETE が返されます。</span><span class="sxs-lookup"><span data-stu-id="61789-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="61789-120">この例では、ブロックに対応するコンポーネントのデコードを停止して、別のコンポーネントが続きますをデコードすること。</span><span class="sxs-lookup"><span data-stu-id="61789-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61789-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="61789-121">See also</span></span>



[<span data-ttu-id="61789-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="61789-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="61789-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="61789-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="61789-124">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="61789-124">MAPI Structures</span></span>](mapi-structures.md)

