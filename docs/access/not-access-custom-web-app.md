---
title: NOT (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0f0a65f-5248-4d7c-a4a4-a0cc863b15ec
description: ブール型 (Boolean) の入力値を反転します。
ms.openlocfilehash: b910613a7bf08c79c2f66a417b5faec4886cb8d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308135"
---
# <a name="not-access-custom-web-app"></a><span data-ttu-id="440c9-103">NOT (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="440c9-103">NOT (Access custom web app)</span></span>

<span data-ttu-id="440c9-104">ブール型 (Boolean) の入力値を反転します。</span><span class="sxs-lookup"><span data-stu-id="440c9-104">Negates a Boolean input.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="440c9-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="440c9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="440c9-107">構文</span><span class="sxs-lookup"><span data-stu-id="440c9-107">Syntax</span></span>

<span data-ttu-id="440c9-108">[ **Not** ]  *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="440c9-108">[ **Not** ]  *BooleanExpression*</span></span> 
  
<span data-ttu-id="440c9-109">**Not** 演算子の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="440c9-109">The **Not** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="440c9-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="440c9-110">**Argument name**</span></span>|<span data-ttu-id="440c9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="440c9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="440c9-112">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="440c9-112">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="440c9-113">有効なブール型 (Boolean) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="440c9-113">A valid Boolean expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="440c9-114">解説</span><span class="sxs-lookup"><span data-stu-id="440c9-114">Remarks</span></span>

<span data-ttu-id="440c9-115">**Not** 演算子を使用して TRUE 値と FALSE 値を比較した場合の結果を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="440c9-115">The following table shows the results of comparing TRUE and FALSE values using the **Not** operator.</span></span> 
  
||<span data-ttu-id="440c9-116">**Not**</span><span class="sxs-lookup"><span data-stu-id="440c9-116">**Not**</span></span>|
|:-----|:-----|
|<span data-ttu-id="440c9-117">**false**</span><span class="sxs-lookup"><span data-stu-id="440c9-117">**TRUE**</span></span> <br/> |<span data-ttu-id="440c9-118">誤り</span><span class="sxs-lookup"><span data-stu-id="440c9-118">False</span></span>  <br/> |
|<span data-ttu-id="440c9-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="440c9-119">**FALSE**</span></span> <br/> |<span data-ttu-id="440c9-120">はい</span><span class="sxs-lookup"><span data-stu-id="440c9-120">True</span></span>  <br/> |
   

