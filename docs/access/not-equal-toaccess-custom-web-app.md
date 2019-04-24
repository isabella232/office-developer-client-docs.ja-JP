---
title: 等しくない (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 687a4200-380d-48ef-85d0-0a2a10d9d87b
description: 2 つの式を比較します。null 以外の式を比較したときに、左のオペランドが右のオペランドと異なる場合、結果は TRUE になり、それ以外の場合、結果は FALSE になります。
localization_priority: Priority
ms.openlocfilehash: 42273a92a8492ea69e7633275454fa7c9ea52b3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308128"
---
# <a name="not-equal-to-access-custom-web-app"></a><span data-ttu-id="9d992-104">等しくない (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="9d992-104">Not Equal To (Access custom web app)</span></span>

<span data-ttu-id="9d992-p102">2 つの式を比較します。null 以外の式を比較したときに、左のオペランドが右のオペランドと異なる場合、結果は TRUE になり、それ以外の場合、結果は FALSE になります。</span><span class="sxs-lookup"><span data-stu-id="9d992-p102">Compares two expressions. When you compare non-null expressions, the result is TRUE if the left operand is not equal to the right operand; otherwise, the result is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9d992-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="9d992-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9d992-109">構文</span><span class="sxs-lookup"><span data-stu-id="9d992-109">Syntax</span></span>

`< > (Not Equal To)`

<span data-ttu-id="9d992-110">*expression*  \<\>  *expression*</span><span class="sxs-lookup"><span data-stu-id="9d992-110">*expression*  \<\>  *expression*</span></span> 
  
<span data-ttu-id="9d992-p104">*expression* は任意の有効な式。いずれの式も、暗黙的に変換可能なデータ型である必要があります。変換は、データ型の優先順位の規則に依存します。</span><span class="sxs-lookup"><span data-stu-id="9d992-p104">*expression*  Is any valid expression. Both expressions must have implicitly convertible data types. The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="9d992-114">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="9d992-114">Return Type</span></span>

<span data-ttu-id="9d992-115">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9d992-115">**Boolean**</span></span>
  

