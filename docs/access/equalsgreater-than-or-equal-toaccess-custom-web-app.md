---
title: 大きいまたは等しい (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cceb8dcb-5ce1-4c32-b057-6201b62a646f
description: 2 つの式を比較して "以上" であるかどうかを判定します。
ms.openlocfilehash: 425745d8634f92e3bcce3cbfcd7d11a890e3be4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798571"
---
# <a name="greater-than-or-equal-to-access-custom-web-app"></a><span data-ttu-id="762c2-103">大きいまたは等しい (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="762c2-103">Greater Than or Equal To (Access custom web app)</span></span>

<span data-ttu-id="762c2-104">2 つの式を比較して "以上" であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="762c2-104">Compares two expressions for greater than or equal.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="762c2-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="762c2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="762c2-107">構文</span><span class="sxs-lookup"><span data-stu-id="762c2-107">Syntax</span></span>

`>= (Greater Than or Equal To)`

<span data-ttu-id="762c2-108">*expression*  \>=  *expression*</span><span class="sxs-lookup"><span data-stu-id="762c2-108">*expression*  \>=  *expression*</span></span> 
  
<span data-ttu-id="762c2-p102">*expression*  任意の有効な式です。式は両方とも、暗黙的に変換可能なデータ型でなければなりません。変換は、データ型の優先順位のルールに依存します。</span><span class="sxs-lookup"><span data-stu-id="762c2-p102">*expression*  Is any valid expression. Both expressions must have implicitly convertible data types. The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="762c2-112">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="762c2-112">Return Type</span></span>

<span data-ttu-id="762c2-113">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="762c2-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="762c2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="762c2-114">Remarks</span></span>

<span data-ttu-id="762c2-115">NULL 以外の式を比較したときに、左側のオペランドの値が右側のオペランドの値以上の場合、結果は TRUE です。それ以外の場合、結果は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="762c2-115">When you compare non-null expressions, the result is TRUE if the left operand has a greater or equal value than the right operand; otherwise, the result is FALSE.</span></span>
  

