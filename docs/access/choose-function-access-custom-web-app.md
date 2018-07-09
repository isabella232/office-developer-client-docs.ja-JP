---
title: 関数 (カスタム web アプリケーションのアクセス) を選択します。
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: 値のリストから、指定されたインデックスの位置にあるアイテムを返します。
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798574"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="6b93b-103">関数 (カスタム web アプリケーションのアクセス) を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b93b-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="6b93b-104">値のリストから、指定されたインデックスの位置にあるアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="6b93b-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6b93b-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="6b93b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6b93b-107">構文</span><span class="sxs-lookup"><span data-stu-id="6b93b-107">Syntax</span></span>

<span data-ttu-id="6b93b-108">**選択**(*IndexNumber**値*を [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="6b93b-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="6b93b-109">**Choose** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6b93b-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6b93b-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="6b93b-110">**Argument name**</span></span>|<span data-ttu-id="6b93b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b93b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6b93b-112">*IndexNumber*</span><span class="sxs-lookup"><span data-stu-id="6b93b-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="6b93b-113">この引数に続くアイテム リストのインデックス (1 から始まるインデックス) を表す整数式。</span><span class="sxs-lookup"><span data-stu-id="6b93b-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="6b93b-114">*値*</span><span class="sxs-lookup"><span data-stu-id="6b93b-114">*Value*</span></span>  <br/> |<span data-ttu-id="6b93b-115">任意のデータ型の値のリスト。</span><span class="sxs-lookup"><span data-stu-id="6b93b-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b93b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6b93b-116">Remarks</span></span>

<span data-ttu-id="6b93b-117">指定された*IndexNumber*が整数でない場合は、値は暗黙的に整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="6b93b-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="6b93b-118">**インデックス値は、値の配列の境界を超えている場合 NULL が返されます。**</span><span class="sxs-lookup"><span data-stu-id="6b93b-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

