---
title: (カスタム web アプリケーションにアクセス) または
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: 2 つの条件を結合します。2 つの条件のいずれかが true の場合に TRUE を返します。
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798707"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="8fd49-104">(カスタム web アプリケーションにアクセス) または</span><span class="sxs-lookup"><span data-stu-id="8fd49-104">OR (Access custom web app)</span></span>

<span data-ttu-id="8fd49-p102">2 つの条件を結合します。2 つの条件のいずれかが true の場合に TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="8fd49-p102">Combines two conditions. Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8fd49-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="8fd49-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8fd49-109">構文</span><span class="sxs-lookup"><span data-stu-id="8fd49-109">Syntax</span></span>

 <span data-ttu-id="8fd49-110">*BooleanExpression* **Or** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="8fd49-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="8fd49-111">**Or** 演算子の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8fd49-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="8fd49-112">**引数名**</span><span class="sxs-lookup"><span data-stu-id="8fd49-112">**Argument name**</span></span>|<span data-ttu-id="8fd49-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="8fd49-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8fd49-114">*ブール式*</span><span class="sxs-lookup"><span data-stu-id="8fd49-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="8fd49-115">TRUE または FALSE を返す任意の有効な式を指定します。</span><span class="sxs-lookup"><span data-stu-id="8fd49-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fd49-116">解説</span><span class="sxs-lookup"><span data-stu-id="8fd49-116">Remarks</span></span>

<span data-ttu-id="8fd49-p104">1 つのステートメント内に複数の論理演算子が使用されている場合、 **Or** 演算子は **And** 演算子の後に評価されます。ただし、かっこを使用すると評価の順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="8fd49-p104">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators. However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="8fd49-119">**Or** 演算子の結果を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="8fd49-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="8fd49-120">**場合は TRUE。**</span><span class="sxs-lookup"><span data-stu-id="8fd49-120">**TRUE**</span></span>|<span data-ttu-id="8fd49-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8fd49-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8fd49-122">**場合は TRUE。**</span><span class="sxs-lookup"><span data-stu-id="8fd49-122">**TRUE**</span></span> <br/> |<span data-ttu-id="8fd49-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="8fd49-123">TRUE</span></span>  <br/> |<span data-ttu-id="8fd49-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="8fd49-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="8fd49-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8fd49-125">**FALSE**</span></span> <br/> |<span data-ttu-id="8fd49-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="8fd49-126">TRUE</span></span>  <br/> |<span data-ttu-id="8fd49-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="8fd49-127">FALSE</span></span>  <br/> |
   

