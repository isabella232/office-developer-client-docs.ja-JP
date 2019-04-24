---
title: IS [NOT] NULL (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: 指定した式が NULL かどうかを判断します。
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311138"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="f451f-103">IS [NOT] NULL (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="f451f-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="f451f-104">指定した式が NULL かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f451f-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f451f-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="f451f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f451f-107">構文</span><span class="sxs-lookup"><span data-stu-id="f451f-107">Syntax</span></span>

 <span data-ttu-id="f451f-108">*expression* **IS** [  *NOT*  ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="f451f-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="f451f-109">**IS [NOT] NULL** 述語には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="f451f-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f451f-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="f451f-110">*expression*</span></span>  <br/> |<span data-ttu-id="f451f-111">任意の有効な式。</span><span class="sxs-lookup"><span data-stu-id="f451f-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="f451f-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="f451f-112">*NOT*</span></span>  <br/> |<span data-ttu-id="f451f-p102">ブール値の結果を否定するように指定します。この述語は、戻り値を反転し、戻り値が NULL でない場合は TRUE が、NULL の場合は FALSE が返されます。</span><span class="sxs-lookup"><span data-stu-id="f451f-p102">Specifies that the Boolean result be negated. The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f451f-115">解説</span><span class="sxs-lookup"><span data-stu-id="f451f-115">Remarks</span></span>

<span data-ttu-id="f451f-116">*expression*  の値が NULL の場合、IS NULL では TRUE が返されます、それ以外の場合は FALSE が返されます。</span><span class="sxs-lookup"><span data-stu-id="f451f-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="f451f-117">式の値が NULL の場合、IS NOT NULL では FALSE が返されます。それ以外の場合は TRUE が返されます。</span><span class="sxs-lookup"><span data-stu-id="f451f-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

