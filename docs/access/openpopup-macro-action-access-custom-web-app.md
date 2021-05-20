---
title: OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: ポップアップ ウィンドウで指定したビューを開きます。
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427389"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="f034a-103">OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="f034a-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f034a-104">ポップアップ ウィンドウで指定したビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="f034a-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f034a-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="f034a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f034a-107">構文</span><span class="sxs-lookup"><span data-stu-id="f034a-107">Syntax</span></span>

 <span data-ttu-id="f034a-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="f034a-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="f034a-109">**OpenPopup アクションには**、次の引数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f034a-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="f034a-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="f034a-110">**Argument name**</span></span>|<span data-ttu-id="f034a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="f034a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f034a-112">*View*</span><span class="sxs-lookup"><span data-stu-id="f034a-112">*View*</span></span>  <br/> |<span data-ttu-id="f034a-113">開くビューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f034a-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="f034a-114">*Where=*</span><span class="sxs-lookup"><span data-stu-id="f034a-114">*Where=*</span></span>  <br/> |<span data-ttu-id="f034a-115">ビュー内SQLを制限する WHERE 句 (WHERE という単語を含む) を指定します。</span><span class="sxs-lookup"><span data-stu-id="f034a-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="f034a-116">*Order By/並び替え*</span><span class="sxs-lookup"><span data-stu-id="f034a-116">*Order By*</span></span>  <br/> |<span data-ttu-id="f034a-p102">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="f034a-p102">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords. By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f034a-119">注釈</span><span class="sxs-lookup"><span data-stu-id="f034a-119">Remarks</span></span>

<span data-ttu-id="f034a-120">OpenPopup アクションが処理 **された後、現在の** マクロは終了します。</span><span class="sxs-lookup"><span data-stu-id="f034a-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="f034a-121">ユーザーが適用した並べ替えまたはフィルター処理は **、OpenPopup** アクションが呼び出されるとクリアされます。</span><span class="sxs-lookup"><span data-stu-id="f034a-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="f034a-p103">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span><span class="sxs-lookup"><span data-stu-id="f034a-p103">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="f034a-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span><span class="sxs-lookup"><span data-stu-id="f034a-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

