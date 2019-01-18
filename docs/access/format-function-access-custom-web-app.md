---
title: Format 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: 指定されたパターンに従って書式設定された値を返します。
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710392"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="bb8af-103">Format 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="bb8af-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="bb8af-104">指定されたパターンに従って書式設定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="bb8af-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bb8af-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="bb8af-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bb8af-107">構文</span><span class="sxs-lookup"><span data-stu-id="bb8af-107">Syntax</span></span>

 <span data-ttu-id="bb8af-108">**Format** (*Expression*, *Format*)</span><span class="sxs-lookup"><span data-stu-id="bb8af-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="bb8af-109">**Format** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bb8af-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="bb8af-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="bb8af-110">**Argument name**</span></span>|<span data-ttu-id="bb8af-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="bb8af-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bb8af-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="bb8af-112">*Expression*</span></span>  <br/> |<span data-ttu-id="bb8af-113">書式設定する、サポートされるデータ型の式</span><span class="sxs-lookup"><span data-stu-id="bb8af-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="bb8af-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="bb8af-114">*Format*</span></span>  <br/> | <span data-ttu-id="bb8af-p102">書式パターン。書式引数には、標準書式文字列 ("C"、"D" など)、または日付や数値用のカスタム文字のパターン ("MMMM dd, yyyy (dddd)" など) として、有効な書式の文字列を含める必要があります。詳細については、「注釈」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb8af-p102">A format pattern. The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)"). For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb8af-118">注釈</span><span class="sxs-lookup"><span data-stu-id="bb8af-118">Remarks</span></span>

<span data-ttu-id="bb8af-119">*Format*  パラメーターでは、以下のパターンのいずれかに一致する文字列を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="bb8af-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="bb8af-120">標準的な数値書式の文字列</span><span class="sxs-lookup"><span data-stu-id="bb8af-120">Standard Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="bb8af-121">カスタムの数値書式の文字列</span><span class="sxs-lookup"><span data-stu-id="bb8af-121">Custom Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="bb8af-122">標準的な日付と時刻の形式の文字列</span><span class="sxs-lookup"><span data-stu-id="bb8af-122">Standard Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="bb8af-123">カスタムの日付と時刻の形式の文字列</span><span class="sxs-lookup"><span data-stu-id="bb8af-123">Custom Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="bb8af-124">Access 2013 Web アプリケーションの以下の領域では、 **Format** 関数を使用できません。</span><span class="sxs-lookup"><span data-stu-id="bb8af-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="bb8af-125">テーブル レベルの集計列</span><span class="sxs-lookup"><span data-stu-id="bb8af-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="bb8af-126">UI マクロ</span><span class="sxs-lookup"><span data-stu-id="bb8af-126">UI macros</span></span>
    
- <span data-ttu-id="bb8af-127">ビュー内の式 (フォーム内など)</span><span class="sxs-lookup"><span data-stu-id="bb8af-127">Expressions in views (for example, in forms)</span></span>
    

