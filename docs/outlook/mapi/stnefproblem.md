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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575330"
---
# <a name="stnefproblem"></a><span data-ttu-id="791dc-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="791dc-103">STnefProblem</span></span>

  
  
<span data-ttu-id="791dc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="791dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="791dc-105">エンコードまたはトランスポート ニュートラル カプセル化形式 (TNEF) ストリームのデコード中に発生するプロパティまたは属性の処理の問題についての情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="791dc-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="791dc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="791dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="791dc-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="791dc-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="791dc-108">Members</span><span class="sxs-lookup"><span data-stu-id="791dc-108">Members</span></span>

 <span data-ttu-id="791dc-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="791dc-109">**ulComponent**</span></span>
  
> <span data-ttu-id="791dc-110">問題が発生した処理の種類です。</span><span class="sxs-lookup"><span data-stu-id="791dc-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="791dc-111">メッセージの処理中に問題が発生した場合は、 **ulComponent**メンバーが 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="791dc-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="791dc-112">添付ファイルの処理中に問題が発生した場合、 **ulComponent**は対応する添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) の値に設定されています。</span><span class="sxs-lookup"><span data-stu-id="791dc-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="791dc-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="791dc-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="791dc-114">プロパティに関連付けられている属性は、 **ulPropTag**のメンバー、または、TNEF の処理の問題が発生したときとカプセル化をデコードすることをブロックする、次のいずれかの示されています。</span><span class="sxs-lookup"><span data-stu-id="791dc-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="791dc-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="791dc-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="791dc-116">メッセージのレベル</span><span class="sxs-lookup"><span data-stu-id="791dc-116">Message level</span></span>
    
 <span data-ttu-id="791dc-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="791dc-117">_attAttachment_</span></span>
  
> <span data-ttu-id="791dc-118">添付ファイルのレベル</span><span class="sxs-lookup"><span data-stu-id="791dc-118">Attachment level</span></span>
    
 <span data-ttu-id="791dc-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="791dc-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="791dc-120">ケース**ulPropTag**が 0 に設定されている、カプセル化、ブロックをデコードするときに問題が発生する場合を除き、TNEF 処理の問題の原因となったプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="791dc-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="791dc-121">**scode**</span><span class="sxs-lookup"><span data-stu-id="791dc-121">**scode**</span></span>
  
> <span data-ttu-id="791dc-122">エラーの処理中に発生した問題を示す値。</span><span class="sxs-lookup"><span data-stu-id="791dc-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="791dc-123">注釈</span><span class="sxs-lookup"><span data-stu-id="791dc-123">Remarks</span></span>

<span data-ttu-id="791dc-124">**STnefProblem**構造体は、属性またはプロパティの処理中に生成されていない場合場合は、アプリケーションがその属性またはプロパティの処理が成功したことを前提として続けることができます。</span><span class="sxs-lookup"><span data-stu-id="791dc-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="791dc-125">唯一の例外は、ブロックをカプセル化のデコード中に問題が発生したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="791dc-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="791dc-126">この例では、ブロックに対応するコンポーネントのデコードを停止して、別のコンポーネントが続きますをデコードすること。</span><span class="sxs-lookup"><span data-stu-id="791dc-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="791dc-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="791dc-127">See also</span></span>



[<span data-ttu-id="791dc-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="791dc-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="791dc-129">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="791dc-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="791dc-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="791dc-130">MAPI Structures</span></span>](mapi-structures.md)

