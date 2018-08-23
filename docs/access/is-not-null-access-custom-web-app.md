---
title: '[しない] が NULL (カスタム web アプリケーションのアクセス)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: 指定した式が NULL かどうかを判別します。
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798583"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="9ba1a-103">[しない] が NULL (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="9ba1a-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="9ba1a-104">指定した式が NULL かどうかを判別します。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9ba1a-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9ba1a-107">構文</span><span class="sxs-lookup"><span data-stu-id="9ba1a-107">Syntax</span></span>

 <span data-ttu-id="9ba1a-108">*expression* **IS** [  *NOT*  ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="9ba1a-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="9ba1a-109">**IS [NOT] NULL** 述語には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ba1a-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="9ba1a-110">*expression*</span></span>  <br/> |<span data-ttu-id="9ba1a-111">任意の有効な式。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="9ba1a-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="9ba1a-112">*NOT*</span></span>  <br/> |<span data-ttu-id="9ba1a-p102">ブール値の結果を否定するように指定します。この述語は、戻り値を反転し、戻り値が NULL でない場合は TRUE が、NULL の場合は FALSE が返されます。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-p102">Specifies that the Boolean result be negated. The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba1a-115">解説</span><span class="sxs-lookup"><span data-stu-id="9ba1a-115">Remarks</span></span>

<span data-ttu-id="9ba1a-116">*expression*  の値が NULL の場合、IS NULL では TRUE が返されます、それ以外の場合は FALSE が返されます。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="9ba1a-117">式の値が NULL の場合、IS NOT NULL では FALSE が返されます。それ以外の場合は TRUE が返されます。</span><span class="sxs-lookup"><span data-stu-id="9ba1a-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

