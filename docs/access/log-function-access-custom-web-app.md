---
title: Log 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: 指定した式の自然対数または指定した値を底とする対数を返します。
ms.openlocfilehash: e2cfd1cf4ad3c1bf44778737faa0f697333f5234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311089"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="5fc3c-103">Log 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="5fc3c-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="5fc3c-104">指定した式の自然対数または指定した値を底とする対数を返します。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5fc3c-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5fc3c-107">構文</span><span class="sxs-lookup"><span data-stu-id="5fc3c-107">Syntax</span></span>

 <span data-ttu-id="5fc3c-108">**ログ**(*NumericExpression* 、[ *Base* ])</span><span class="sxs-lookup"><span data-stu-id="5fc3c-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="5fc3c-109">**Log** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5fc3c-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="5fc3c-110">**Argument name**</span></span>|<span data-ttu-id="5fc3c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5fc3c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5fc3c-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="5fc3c-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="5fc3c-113">対数が返される正の値。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="5fc3c-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="5fc3c-114">*Base*</span></span>  <br/> |<span data-ttu-id="5fc3c-115">対数の底。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-115">The base of the logarithm.</span></span> <span data-ttu-id="5fc3c-116">省略すると、 **Log**関数は自然対数を返します。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fc3c-117">解説</span><span class="sxs-lookup"><span data-stu-id="5fc3c-117">Remarks</span></span>

<span data-ttu-id="5fc3c-118">類似する **Log10** 関数では、常に底が 10 である常用対数が返されます。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="5fc3c-119">自然対数は、底 e を底とする対数です。ここで、e は2.718281828 とほぼ等しくなる irrational 定数です。</span><span class="sxs-lookup"><span data-stu-id="5fc3c-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

