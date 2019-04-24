---
title: Count 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: クエリまたはテーブルに含まれるレコードの数が返されます。
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282237"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="b5903-103">Count 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="b5903-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="b5903-104">クエリまたはテーブルに含まれるレコードの数が返されます。</span><span class="sxs-lookup"><span data-stu-id="b5903-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b5903-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="b5903-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b5903-107">構文</span><span class="sxs-lookup"><span data-stu-id="b5903-107">Syntax</span></span>

<span data-ttu-id="b5903-108">**Count**(*式*)</span><span class="sxs-lookup"><span data-stu-id="b5903-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="b5903-109">**Count** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="b5903-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="b5903-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="b5903-110">**Argument name**</span></span>|<span data-ttu-id="b5903-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5903-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b5903-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="b5903-112">*Expression*</span></span>  <br/> |<span data-ttu-id="b5903-113">計算するデータを含むフィールドを識別する文字列式、またはフィールドのデータを使用して計算を実行する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5903-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="b5903-114">*Expression*のオペランドには、テーブルのフィールドまたは関数の名前を含めることができます (組み込みまたはユーザー定義であっても、他の SQL 集計関数は使用できません)。</span><span class="sxs-lookup"><span data-stu-id="b5903-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="b5903-115">テキストを含む任意の種類のデータをカウントできます。</span><span class="sxs-lookup"><span data-stu-id="b5903-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5903-116">解説</span><span class="sxs-lookup"><span data-stu-id="b5903-116">Remarks</span></span>

<span data-ttu-id="b5903-p103">Count 関数を使用すると、元になるクエリのレコード数をカウントできます。たとえば、Count 関数を使用して、特定の国または地域に出荷された注文の数をカウントできます。</span><span class="sxs-lookup"><span data-stu-id="b5903-p103">You can use Count to count the number of records in an underlying query. For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="b5903-p104">**Count** (\*) では、グループ内の項目数が返されます。NULL 値および重複する値もカウントされます。</span><span class="sxs-lookup"><span data-stu-id="b5903-p104">**Count** (\*) returns the number of items in a group. This includes NULL values and duplicates.</span></span> 
  

