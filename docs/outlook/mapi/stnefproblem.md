---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435181"
---
# <a name="stnefproblem"></a><span data-ttu-id="e084b-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="e084b-103">STnefProblem</span></span>

  
  
<span data-ttu-id="e084b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e084b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e084b-105">トランスポートニュートラルカプセル化形式 (TNEF) ストリームのエンコードまたはデコード中に発生したプロパティまたは属性処理の問題に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e084b-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e084b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e084b-106">Header file:</span></span>  <br/> |<span data-ttu-id="e084b-107">Tnef</span><span class="sxs-lookup"><span data-stu-id="e084b-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="e084b-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="e084b-108">Members</span></span>

 <span data-ttu-id="e084b-109">**ulcomponent**</span><span class="sxs-lookup"><span data-stu-id="e084b-109">**ulComponent**</span></span>
  
> <span data-ttu-id="e084b-110">問題が発生した処理の種類。</span><span class="sxs-lookup"><span data-stu-id="e084b-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="e084b-111">メッセージ処理中に問題が発生した場合、 **ulcomponent**メンバーは0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e084b-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="e084b-112">添付ファイルの処理中に問題が発生した場合、 **ulcomponent**は対応する添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e084b-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="e084b-113">**ulattribute**</span><span class="sxs-lookup"><span data-stu-id="e084b-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="e084b-114">属性。 **ulPropTag**メンバーによって示されるプロパティに関連付けられている属性。または、カプセル化ブロックのデコード時に TNEF 処理の問題が発生した場合は、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="e084b-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="e084b-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="e084b-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="e084b-116">メッセージレベル</span><span class="sxs-lookup"><span data-stu-id="e084b-116">Message level</span></span>
    
 <span data-ttu-id="e084b-117">_添付ファイル_</span><span class="sxs-lookup"><span data-stu-id="e084b-117">_attAttachment_</span></span>
  
> <span data-ttu-id="e084b-118">添付ファイルレベル</span><span class="sxs-lookup"><span data-stu-id="e084b-118">Attachment level</span></span>
    
 <span data-ttu-id="e084b-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e084b-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="e084b-120">**ulPropTag**が0に設定されている場合を除き、TNEF 処理の問題の原因となったプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="e084b-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="e084b-121">**scode as scode**</span><span class="sxs-lookup"><span data-stu-id="e084b-121">**scode**</span></span>
  
> <span data-ttu-id="e084b-122">処理中に発生した問題を示すエラー値。</span><span class="sxs-lookup"><span data-stu-id="e084b-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e084b-123">注釈</span><span class="sxs-lookup"><span data-stu-id="e084b-123">Remarks</span></span>

<span data-ttu-id="e084b-124">属性またはプロパティの処理中に**STnefProblem**構造体が生成されない場合、アプリケーションは、その属性またはプロパティの処理が正常に終了したことを前提として続行できます。</span><span class="sxs-lookup"><span data-stu-id="e084b-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="e084b-125">唯一の例外は、カプセル化ブロックのデコード中に問題が発生した場合です。</span><span class="sxs-lookup"><span data-stu-id="e084b-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="e084b-126">この場合、ブロックに対応するコンポーネントのデコードが停止され、別のコンポーネントでデコードが続行されます。</span><span class="sxs-lookup"><span data-stu-id="e084b-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e084b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e084b-127">See also</span></span>



[<span data-ttu-id="e084b-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="e084b-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="e084b-129">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e084b-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="e084b-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e084b-130">MAPI Structures</span></span>](mapi-structures.md)

