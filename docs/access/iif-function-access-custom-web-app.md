---
title: IIf 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: 条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439080"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="41662-103">IIf 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="41662-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="41662-104">条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。</span><span class="sxs-lookup"><span data-stu-id="41662-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="41662-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="41662-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="41662-107">構文</span><span class="sxs-lookup"><span data-stu-id="41662-107">Syntax</span></span>

<span data-ttu-id="41662-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="41662-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="41662-109">**IIf** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="41662-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="41662-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="41662-110">**Argument name**</span></span>|<span data-ttu-id="41662-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="41662-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="41662-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="41662-112">*Condition*</span></span>  <br/> |<span data-ttu-id="41662-113">評価する式。</span><span class="sxs-lookup"><span data-stu-id="41662-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="41662-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="41662-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="41662-115">Condition が True の場合に返  *される値*  または式。</span><span class="sxs-lookup"><span data-stu-id="41662-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="41662-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="41662-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="41662-117">Condition が False の場合に返  *される値*  または式。</span><span class="sxs-lookup"><span data-stu-id="41662-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="41662-118">例</span><span class="sxs-lookup"><span data-stu-id="41662-118">Example</span></span>

<span data-ttu-id="41662-119">テーブルに FirstName、MiddleInitial、および LastName の各フィールドが含まれる場合、次の式を使用して人のフル ネームを表示できます。</span><span class="sxs-lookup"><span data-stu-id="41662-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="41662-120">MiddleInitial フィールドが空白の場合、完全な名前を表示するには、FirstName フィールドと LastName フィールドだけが結合されます。</span><span class="sxs-lookup"><span data-stu-id="41662-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


