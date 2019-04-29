---
title: OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: 指定したビューをポップアップウィンドウで開きます。
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427389"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="e91e9-103">OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="e91e9-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="e91e9-104">指定したビューをポップアップウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="e91e9-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e91e9-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="e91e9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e91e9-107">構文</span><span class="sxs-lookup"><span data-stu-id="e91e9-107">Syntax</span></span>

 <span data-ttu-id="e91e9-108">**openpopup**(*ビュー*、 *Where =*、 *Order By*)</span><span class="sxs-lookup"><span data-stu-id="e91e9-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="e91e9-109">**openpopup**アクションには、次の引数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e91e9-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="e91e9-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="e91e9-110">**Argument name**</span></span>|<span data-ttu-id="e91e9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e91e9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e91e9-112">*View*</span><span class="sxs-lookup"><span data-stu-id="e91e9-112">*View*</span></span>  <br/> |<span data-ttu-id="e91e9-113">開くビューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e91e9-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="e91e9-114">*Where =*</span><span class="sxs-lookup"><span data-stu-id="e91e9-114">*Where=*</span></span>  <br/> |<span data-ttu-id="e91e9-115">ビュー内のレコードを制限する有効な SQL where 句 (単語 where を除く)。</span><span class="sxs-lookup"><span data-stu-id="e91e9-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="e91e9-116">*Order By/並び替え*</span><span class="sxs-lookup"><span data-stu-id="e91e9-116">*Order By*</span></span>  <br/> |<span data-ttu-id="e91e9-p102">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="e91e9-p102">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords. By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e91e9-119">注釈</span><span class="sxs-lookup"><span data-stu-id="e91e9-119">Remarks</span></span>

<span data-ttu-id="e91e9-120">**openpopup**アクションが処理されると、現在のマクロは終了します。</span><span class="sxs-lookup"><span data-stu-id="e91e9-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="e91e9-121">**openpopup**アクションが呼び出されると、ユーザーによって適用されたすべての並べ替えまたはフィルター処理がクリアされます。</span><span class="sxs-lookup"><span data-stu-id="e91e9-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="e91e9-p103">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span><span class="sxs-lookup"><span data-stu-id="e91e9-p103">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="e91e9-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span><span class="sxs-lookup"><span data-stu-id="e91e9-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

