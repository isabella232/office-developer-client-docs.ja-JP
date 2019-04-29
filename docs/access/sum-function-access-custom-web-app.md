---
title: Sum 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: 式に含まれるすべての値の合計が返されます。
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427102"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="36e4e-103">Sum 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="36e4e-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="36e4e-104">式に含まれるすべての値の合計が返されます。</span><span class="sxs-lookup"><span data-stu-id="36e4e-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="36e4e-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="36e4e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36e4e-107">構文</span><span class="sxs-lookup"><span data-stu-id="36e4e-107">Syntax</span></span>

 <span data-ttu-id="36e4e-108">**合計**(*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="36e4e-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="36e4e-109">**Sum** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="36e4e-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="36e4e-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="36e4e-110">**Argument name**</span></span>|<span data-ttu-id="36e4e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="36e4e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36e4e-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="36e4e-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="36e4e-113">追加する数値データを含むフィールドを識別する式、またはそのフィールドのデータを使用して計算を実行する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="36e4e-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="36e4e-114">*NumericExpression*のオペランドには、テーブルフィールドの名前、定数、または関数を含めることができます (組み込みまたはユーザー定義であっても、他の SQL 集計関数は使用できません)。</span><span class="sxs-lookup"><span data-stu-id="36e4e-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36e4e-115">注釈</span><span class="sxs-lookup"><span data-stu-id="36e4e-115">Remarks</span></span>

<span data-ttu-id="36e4e-116">**Sum** 関数は、Null 値が含まれるレコードを無視します。</span><span class="sxs-lookup"><span data-stu-id="36e4e-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="36e4e-117">**Sum** 関数は、数値列でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="36e4e-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

