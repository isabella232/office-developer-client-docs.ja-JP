---
title: GoToControl マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: GoToControl /コントロールの移動アクションを使用すると、開いているビューの現在のレコード内の指定したコントロールにフォーカスを移動できます。
ms.openlocfilehash: ec156d1eb6c510ee38c0268a7b0f51bdde80f887
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798568"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a><span data-ttu-id="db8da-103">GoToControl マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="db8da-103">GoToControl Macro Action (Access custom web app)</span></span>

<span data-ttu-id="db8da-104">" **GoToControl** /コントロールの移動" アクションを使用すると、開いているビューの現在のレコード内の指定したコントロールにフォーカスを移動できます。</span><span class="sxs-lookup"><span data-stu-id="db8da-104">You can use the **GoToControl** action to move the focus to the specified control in the current record of the open view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="db8da-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="db8da-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="db8da-107">設定</span><span class="sxs-lookup"><span data-stu-id="db8da-107">Setting</span></span>

<span data-ttu-id="db8da-108">" **GoToControl** /コントロールの移動" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="db8da-108">The **GoToControl** action has the following argument.</span></span> 
  
|<span data-ttu-id="db8da-109">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="db8da-109">**Action argument**</span></span>|<span data-ttu-id="db8da-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="db8da-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db8da-111">**Control Name/コントロール名**</span><span class="sxs-lookup"><span data-stu-id="db8da-111">**Control Name**</span></span> <br/> |<span data-ttu-id="db8da-p102">フォーカスの移動先のフィールドまたはコントロールの名前。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="db8da-p102">The name of the field or control where you want the focus. This is a required argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db8da-114">注釈</span><span class="sxs-lookup"><span data-stu-id="db8da-114">Remarks</span></span>

<span data-ttu-id="db8da-p103">特定のフィールドまたはコントロールにフォーカスを移動する必要がある場合にこのアクションを使用できます。また、このアクションを使用して、特定の条件に従ってフォーム内をナビゲーションできます。たとえば、医療保険のフォームでユーザーが [既婚] コントロールに [いいえ] と入力した場合、[配偶者またはパートナーの名前] コントロールを自動的にスキップしてフォーカスを次のコントロールに移動できます。</span><span class="sxs-lookup"><span data-stu-id="db8da-p103">You can use this action when you want a particular field or control to have the focus. You can also use this action to navigate in a form according to certain conditions. For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>
  

