---
title: または (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: 2 つの条件を結合します。 2 つの条件のいずれかが true の場合に TRUE を返します。
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414761"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="145fc-104">または (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="145fc-104">OR (Access custom web app)</span></span>

<span data-ttu-id="145fc-105">2 つの条件を結合します。</span><span class="sxs-lookup"><span data-stu-id="145fc-105">Combines two conditions.</span></span> <span data-ttu-id="145fc-106">2 つの条件のいずれかが true の場合に TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="145fc-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="145fc-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="145fc-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="145fc-109">構文</span><span class="sxs-lookup"><span data-stu-id="145fc-109">Syntax</span></span>

 <span data-ttu-id="145fc-110">*BooleanExpression* **Or** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="145fc-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="145fc-111">**Or** 演算子の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="145fc-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="145fc-112">**引数名**</span><span class="sxs-lookup"><span data-stu-id="145fc-112">**Argument name**</span></span>|<span data-ttu-id="145fc-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="145fc-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="145fc-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="145fc-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="145fc-115">TRUE または FALSE を返す任意の有効な式を指定します。</span><span class="sxs-lookup"><span data-stu-id="145fc-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="145fc-116">注釈</span><span class="sxs-lookup"><span data-stu-id="145fc-116">Remarks</span></span>

<span data-ttu-id="145fc-p104">1 つのステートメント内に複数の論理演算子が使用されている場合、 **Or** 演算子は **And** 演算子の後に評価されます。ただし、かっこを使用すると評価の順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="145fc-p104">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators. However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="145fc-119">**Or** 演算子の結果を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="145fc-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="145fc-120">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="145fc-120">**TRUE**</span></span>|<span data-ttu-id="145fc-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="145fc-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="145fc-122">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="145fc-122">**TRUE**</span></span> <br/> |<span data-ttu-id="145fc-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="145fc-123">TRUE</span></span>  <br/> |<span data-ttu-id="145fc-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="145fc-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="145fc-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="145fc-125">**FALSE**</span></span> <br/> |<span data-ttu-id="145fc-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="145fc-126">TRUE</span></span>  <br/> |<span data-ttu-id="145fc-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="145fc-127">FALSE</span></span>  <br/> |
   

