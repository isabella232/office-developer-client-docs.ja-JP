---
title: SetReturnVar マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: SetReturnVar/戻り変数の設定アクションは、戻り変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798758"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="31a08-103">SetReturnVar マクロのアクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="31a08-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="31a08-104">" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="31a08-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="31a08-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="31a08-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="31a08-107">[!メモ] " **SetReturnVar/戻り変数の設定** " アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="31a08-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="31a08-108">設定</span><span class="sxs-lookup"><span data-stu-id="31a08-108">Setting</span></span>

<span data-ttu-id="31a08-109">" **SetReturnVar/戻り変数の設定** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="31a08-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="31a08-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="31a08-110">**Argument name**</span></span>|<span data-ttu-id="31a08-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="31a08-111">**Required**</span></span>|<span data-ttu-id="31a08-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a08-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="31a08-113">_名前_</span><span class="sxs-lookup"><span data-stu-id="31a08-113">_Name_</span></span> <br/> |<span data-ttu-id="31a08-114">はい</span><span class="sxs-lookup"><span data-stu-id="31a08-114">Yes</span></span>  <br/> |<span data-ttu-id="31a08-115">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="31a08-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="31a08-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="31a08-116">_Expression_</span></span> <br/> |<span data-ttu-id="31a08-117">はい</span><span class="sxs-lookup"><span data-stu-id="31a08-117">Yes</span></span>  <br/> |<span data-ttu-id="31a08-118">この一時変数の値を設定に使用する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="31a08-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="31a08-119">式の前に等号 (=) を付けないでください。</span><span class="sxs-lookup"><span data-stu-id="31a08-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="31a08-120">この引数を設定するのには、**式ビルダー**を使用するのには [**ビルド**] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="31a08-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31a08-121">注釈</span><span class="sxs-lookup"><span data-stu-id="31a08-121">Remarks</span></span>

<span data-ttu-id="31a08-122">" **SetReturnVar/戻り変数の設定** " アクションを使用して、 **ReturnVar** を作成します。この変数は、" **RunDataMacro/データマクロの実行** " アクションを使用してデータ マクロを呼び出すマクロが使用できます。</span><span class="sxs-lookup"><span data-stu-id="31a08-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="31a08-123">**SetReturnVar**アクションによって、 **ReturnVar**が作成されると、呼び出し元のマクロで使用できます、式。</span><span class="sxs-lookup"><span data-stu-id="31a08-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="31a08-124">たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="31a08-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="31a08-p104">" **SetReturnVar** /戻り変数の設定" アクションは、名前付きのデータ マクロでのみ使用できます。これを、データ マクロ イベントに接続されたデータ マクロで使用できません。</span><span class="sxs-lookup"><span data-stu-id="31a08-p104">The **SetReturnVar** action can be used only in named data macros. It is not available in data macros that are attached to a data macro event.</span></span> 
  

