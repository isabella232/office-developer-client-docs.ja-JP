---
title: changeview マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: ChangeView /ビューの変更アクションを使用して、ビュー間を移動できます。
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282314"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="e4dc0-103">changeview マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="e4dc0-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="e4dc0-104">" **ChangeView** /ビューの変更" アクションを使用して、ビュー間を移動できます。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e4dc0-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="e4dc0-107">設定</span><span class="sxs-lookup"><span data-stu-id="e4dc0-107">Setting</span></span>

<span data-ttu-id="e4dc0-108">"**ChangeView**/ビューの変更" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="e4dc0-109">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="e4dc0-109">**Action argument**</span></span>|<span data-ttu-id="e4dc0-110">**必須**</span><span class="sxs-lookup"><span data-stu-id="e4dc0-110">**Required**</span></span>|<span data-ttu-id="e4dc0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e4dc0-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4dc0-112">Table</span><span class="sxs-lookup"><span data-stu-id="e4dc0-112">Table</span></span>  <br/> |<span data-ttu-id="e4dc0-113">はい</span><span class="sxs-lookup"><span data-stu-id="e4dc0-113">Yes</span></span>  <br/> |<span data-ttu-id="e4dc0-114">開くテーブル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="e4dc0-115">View</span><span class="sxs-lookup"><span data-stu-id="e4dc0-115">View</span></span>  <br/> |<span data-ttu-id="e4dc0-116">はい</span><span class="sxs-lookup"><span data-stu-id="e4dc0-116">Yes</span></span>  <br/> |<span data-ttu-id="e4dc0-117">開くビューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="e4dc0-118">ここで</span><span class="sxs-lookup"><span data-stu-id="e4dc0-118">Where</span></span>  <br/> |<span data-ttu-id="e4dc0-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="e4dc0-119">No</span></span>  <br/> |<span data-ttu-id="e4dc0-120">指定した場合は、オブジェクト レコード ソースの Where 条件式を置換します。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="e4dc0-121">Order By</span><span class="sxs-lookup"><span data-stu-id="e4dc0-121">Order By</span></span>  <br/> |<span data-ttu-id="e4dc0-122">いいえ</span><span class="sxs-lookup"><span data-stu-id="e4dc0-122">No</span></span>  <br/> |<span data-ttu-id="e4dc0-p102">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-p102">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords. By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4dc0-125">解説</span><span class="sxs-lookup"><span data-stu-id="e4dc0-125">Remarks</span></span>

<span data-ttu-id="e4dc0-126">ユーザーが適用したすべての並べ替えまたはフィルター処理は、" **ChangeView** /ビューの変更" アクションが呼び出されるとクリアされます。</span><span class="sxs-lookup"><span data-stu-id="e4dc0-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="e4dc0-p103">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span><span class="sxs-lookup"><span data-stu-id="e4dc0-p103">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="e4dc0-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span><span class="sxs-lookup"><span data-stu-id="e4dc0-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

