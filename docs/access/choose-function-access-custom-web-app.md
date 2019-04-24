---
title: Choose function (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: 値のリストから、指定されたインデックスの位置にあるアイテムを返します。
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282286"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="b3e78-103">Choose function (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="b3e78-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="b3e78-104">値のリストから、指定されたインデックスの位置にあるアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="b3e78-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b3e78-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="b3e78-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b3e78-107">構文</span><span class="sxs-lookup"><span data-stu-id="b3e78-107">Syntax</span></span>

<span data-ttu-id="b3e78-108">**[**(*indexnumber*, *Value*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="b3e78-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="b3e78-109">**Choose** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b3e78-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b3e78-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="b3e78-110">**Argument name**</span></span>|<span data-ttu-id="b3e78-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b3e78-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b3e78-112">*indexnumber*</span><span class="sxs-lookup"><span data-stu-id="b3e78-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="b3e78-113">この引数に続くアイテム リストのインデックス (1 から始まるインデックス) を表す整数式。</span><span class="sxs-lookup"><span data-stu-id="b3e78-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="b3e78-114">*値*</span><span class="sxs-lookup"><span data-stu-id="b3e78-114">*Value*</span></span>  <br/> |<span data-ttu-id="b3e78-115">任意のデータ型の値のリスト。</span><span class="sxs-lookup"><span data-stu-id="b3e78-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3e78-116">解説</span><span class="sxs-lookup"><span data-stu-id="b3e78-116">Remarks</span></span>

<span data-ttu-id="b3e78-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span><span class="sxs-lookup"><span data-stu-id="b3e78-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="b3e78-118">インデックス値が値の配列の範囲を超える場合、 **Choose**は NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="b3e78-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

