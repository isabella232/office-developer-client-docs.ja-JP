---
title: Equals (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: 2 つの値が等しいかどうかを比較します。
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308226"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="2e099-103">Equals (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="2e099-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="2e099-104">2 つの値が等しいかどうかを比較します。</span><span class="sxs-lookup"><span data-stu-id="2e099-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2e099-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="2e099-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2e099-107">構文</span><span class="sxs-lookup"><span data-stu-id="2e099-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="2e099-108">*expression*  =  *expression*</span><span class="sxs-lookup"><span data-stu-id="2e099-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="2e099-p102">*expression*  は任意の有効な式です。これらの式のデータ型が異なる場合、一方のデータ型に、もう一方のデータ型に暗黙的に変換可能なデータ型を使用する必要があります。変換はデータ型の優先順位の規則によって決まります。</span><span class="sxs-lookup"><span data-stu-id="2e099-p102">*expression*  Is any valid expression. If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other. The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="2e099-112">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="2e099-112">Return Type</span></span>

<span data-ttu-id="2e099-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2e099-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e099-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2e099-114">Remarks</span></span>

<span data-ttu-id="2e099-115">2 つの NULL 式を比較した場合、結果は TRUE になります。</span><span class="sxs-lookup"><span data-stu-id="2e099-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="2e099-116">NULL 値を NULL 以外の値と比較した場合、結果は常に FALSE になります。</span><span class="sxs-lookup"><span data-stu-id="2e099-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

