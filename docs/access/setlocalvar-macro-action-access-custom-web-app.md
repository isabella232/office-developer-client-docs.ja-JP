---
title: 予約マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: SetLocalVar/ローカル変数の設定アクションは、一時変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: 26b1515a8604c02c32135e6e5ccf6fe1e67622f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19798732"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="46449-103">予約マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="46449-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="46449-104">" **SetLocalVar/ローカル変数の設定** " アクションは、一時変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="46449-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="46449-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="46449-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="46449-107">" **SetLocalVar/ローカル変数の設定** " アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="46449-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="46449-108">設定</span><span class="sxs-lookup"><span data-stu-id="46449-108">Setting</span></span>

<span data-ttu-id="46449-109">" **SetLocalVar/ローカル変数の設定** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="46449-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="46449-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="46449-110">**Argument name**</span></span>|<span data-ttu-id="46449-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="46449-111">**Required**</span></span>|<span data-ttu-id="46449-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="46449-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46449-113">**名前**</span><span class="sxs-lookup"><span data-stu-id="46449-113">**Name**</span></span> <br/> |<span data-ttu-id="46449-114">はい</span><span class="sxs-lookup"><span data-stu-id="46449-114">Yes</span></span>  <br/> |<span data-ttu-id="46449-115">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="46449-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="46449-116">**Expression**</span><span class="sxs-lookup"><span data-stu-id="46449-116">**Expression**</span></span> <br/> |<span data-ttu-id="46449-117">はい</span><span class="sxs-lookup"><span data-stu-id="46449-117">Yes</span></span>  <br/> |<span data-ttu-id="46449-118">この一時変数の値を設定に使用する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="46449-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="46449-119">式の前に等号 (=) を付けないでください。</span><span class="sxs-lookup"><span data-stu-id="46449-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="46449-120">この引数を設定するのには、**式ビルダー**を使用するのには [**ビルド**] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="46449-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   

