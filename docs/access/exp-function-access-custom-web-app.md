---
title: Exp 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: 指定した式の指数値を戻します。
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798558"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="22cb1-103">Exp 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="22cb1-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="22cb1-104">指定した式の指数値を戻します。</span><span class="sxs-lookup"><span data-stu-id="22cb1-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="22cb1-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="22cb1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="22cb1-107">構文</span><span class="sxs-lookup"><span data-stu-id="22cb1-107">Syntax</span></span>

 <span data-ttu-id="22cb1-108">**Exp**(*数式*)</span><span class="sxs-lookup"><span data-stu-id="22cb1-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="22cb1-109">**Exp** 関数には以下の引数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="22cb1-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="22cb1-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="22cb1-110">**Argument name**</span></span>|<span data-ttu-id="22cb1-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="22cb1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="22cb1-112">*数式*</span><span class="sxs-lookup"><span data-stu-id="22cb1-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="22cb1-113">Double 型、または Double に暗黙的に変換できる式。</span><span class="sxs-lookup"><span data-stu-id="22cb1-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22cb1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="22cb1-114">Remarks</span></span>

<span data-ttu-id="22cb1-115">定数 **e** (2.718281...) は、自然対数の基数です。</span><span class="sxs-lookup"><span data-stu-id="22cb1-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="22cb1-p102">ある数値の指数とは、定数 **e** をべき乗する数値です。たとえば、 **Exp** (1.0) = e^1.0 = 2.71828182845905 となり、 **Exp** (10) = e^10 = 22026.4657948067 となります。</span><span class="sxs-lookup"><span data-stu-id="22cb1-p102">The exponent of a number is the constant **e** raised to the power of the number. For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="22cb1-118">数値の自然対数の指数は、番号自体: **Exp** (LOG (n)) = n です。</span><span class="sxs-lookup"><span data-stu-id="22cb1-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="22cb1-119">数値の指数の自然対数は、番号自体: ログ (**Exp** (n)) = n です。</span><span class="sxs-lookup"><span data-stu-id="22cb1-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

