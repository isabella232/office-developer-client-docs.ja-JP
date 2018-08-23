---
title: OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: ポップアップ ・ ウィンドウで指定されたビューを開きます。
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798706"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="40967-103">OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="40967-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="40967-104">ポップアップ ・ ウィンドウで指定されたビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="40967-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="40967-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="40967-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="40967-107">構文</span><span class="sxs-lookup"><span data-stu-id="40967-107">Syntax</span></span>

 <span data-ttu-id="40967-108">**OpenPopup**(*ビュー*、 *、=*、*順*)</span><span class="sxs-lookup"><span data-stu-id="40967-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="40967-109">**OpenPopup**アクションには、次の引数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="40967-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="40967-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="40967-110">**Argument name**</span></span>|<span data-ttu-id="40967-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="40967-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="40967-112">*View*</span><span class="sxs-lookup"><span data-stu-id="40967-112">*View*</span></span>  <br/> |<span data-ttu-id="40967-113">開くビューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="40967-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="40967-114">*場所 =*</span><span class="sxs-lookup"><span data-stu-id="40967-114">*Where=*</span></span>  <br/> |<span data-ttu-id="40967-115">有効な SQL WHERE 句 (単語なしで) ビュー内のレコードを制限しています。</span><span class="sxs-lookup"><span data-stu-id="40967-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="40967-116">*Order By/並び替え*</span><span class="sxs-lookup"><span data-stu-id="40967-116">*Order By*</span></span>  <br/> |<span data-ttu-id="40967-p102">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="40967-p102">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords. By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40967-119">注釈</span><span class="sxs-lookup"><span data-stu-id="40967-119">Remarks</span></span>

<span data-ttu-id="40967-120">**OpenPopup**アクションを処理すると、現在のマクロが終了します。</span><span class="sxs-lookup"><span data-stu-id="40967-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="40967-121">**OpenPopup**アクションが呼び出されたときに、並べ替え、またはユーザーによって適用されたフィルターがクリアされます。</span><span class="sxs-lookup"><span data-stu-id="40967-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="40967-122">*並べ替え*引数は、フィールドまたはレコードをソートするフィールドの名前です。</span><span class="sxs-lookup"><span data-stu-id="40967-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="40967-123">複数のフィールド名を指定する場合はコンマ (,) で区切ります。</span><span class="sxs-lookup"><span data-stu-id="40967-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="40967-124">*並べ替え*引数を設定すると、既定では昇順でレコードが並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="40967-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

