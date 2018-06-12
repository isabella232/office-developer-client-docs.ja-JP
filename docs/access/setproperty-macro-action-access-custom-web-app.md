---
title: SetProperty マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: SetProperty/プロパティの設定アクションを使用して、ビュー上のコントロールのプロパティを設定できます。
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798729"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="ae030-103">SetProperty マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="ae030-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ae030-104">" **SetProperty/プロパティの設定** " アクションを使用して、ビュー上のコントロールのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ae030-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ae030-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="ae030-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ae030-107">設定</span><span class="sxs-lookup"><span data-stu-id="ae030-107">Setting</span></span>

<span data-ttu-id="ae030-108">" **SetField/フィールドの設定** " アクションには、以下の表に示す引数があります。</span><span class="sxs-lookup"><span data-stu-id="ae030-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="ae030-109">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="ae030-109">**Action argument**</span></span>|<span data-ttu-id="ae030-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae030-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ae030-111">_Control Name/コントロール名_</span><span class="sxs-lookup"><span data-stu-id="ae030-111">_Control Name_</span></span> <br/> |<span data-ttu-id="ae030-p102">プロパティ値を設定する対象のフィールドまたはコントロールの名前を指定します。ビューのプロパティを設定する場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="ae030-p102">Type the name of the field or control for which you want to set the property value. Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="ae030-114">_プロパティ_</span><span class="sxs-lookup"><span data-stu-id="ae030-114">_Property_</span></span> <br/> |<span data-ttu-id="ae030-115">設定するプロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae030-115">Select the property that you want to set.</span></span> <span data-ttu-id="ae030-116">このアクションを使用して設定できるプロパティの一覧については、この資料の **「解説」** セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae030-116">See the **Remarks** section in this article for a list of the properties that can be set by using this action.</span></span>  <br/> |
| <span data-ttu-id="ae030-117">_値_</span><span class="sxs-lookup"><span data-stu-id="ae030-117">_Value_</span></span> <br/> |<span data-ttu-id="ae030-118">プロパティを設定する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae030-118">Type the value that the property is to be set to.</span></span> <span data-ttu-id="ae030-119">プロパティの値を持つか、[はい] またはいいえ、 **-1**を使用して、[はい] を [いいえ] は**0**</span><span class="sxs-lookup"><span data-stu-id="ae030-119">For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae030-120">注釈</span><span class="sxs-lookup"><span data-stu-id="ae030-120">Remarks</span></span>

<span data-ttu-id="ae030-121">" **SetProperty/プロパティの設定** " アクションを使用して、コントロールの以下のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ae030-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="ae030-122">Caption</span><span class="sxs-lookup"><span data-stu-id="ae030-122">Caption</span></span>
    
- <span data-ttu-id="ae030-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="ae030-123">Enabled</span></span>
    
- <span data-ttu-id="ae030-124">前景色</span><span class="sxs-lookup"><span data-stu-id="ae030-124">ForeColor</span></span>
    
- <span data-ttu-id="ae030-125">Value</span><span class="sxs-lookup"><span data-stu-id="ae030-125">Value</span></span>
    
- <span data-ttu-id="ae030-126">Visible</span><span class="sxs-lookup"><span data-stu-id="ae030-126">Visible</span></span>
    
<span data-ttu-id="ae030-127">" *Value/値* " 引数に無効な値を入力すると、エラーは発生しませんが、引数がどのように解釈されるかに応じて、プロパティは別の値に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae030-127">If you enter an invalid value for the ** *Value* ** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

