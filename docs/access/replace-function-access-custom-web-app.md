---
title: Replace 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 93c8fc1d-e70c-4726-af2f-c6501d82e49b
description: 指定した文字列値のすべての一致箇所を別の文字列値に置換します。
ms.openlocfilehash: 678cf88fe66d65be454613ce2c615bb7cb8f66d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308002"
---
# <a name="replace-function-access-custom-web-app"></a><span data-ttu-id="a7667-103">Replace 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="a7667-103">Replace Function (Access custom web app)</span></span>

<span data-ttu-id="a7667-104">指定した文字列値のすべての一致箇所を別の文字列値に置換します。</span><span class="sxs-lookup"><span data-stu-id="a7667-104">Replaces all occurrences of a specified string value with another string value.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a7667-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="a7667-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a7667-107">構文</span><span class="sxs-lookup"><span data-stu-id="a7667-107">Syntax</span></span>

 <span data-ttu-id="a7667-108">**Replace**(*textexpression*, *Pattern*, *Replacement*)</span><span class="sxs-lookup"><span data-stu-id="a7667-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span></span> 
  
<span data-ttu-id="a7667-109">**Replace** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a7667-109">The **Replace** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a7667-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="a7667-110">**Argument name**</span></span>|<span data-ttu-id="a7667-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a7667-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a7667-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="a7667-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="a7667-113">検索する文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7667-113">The string expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="a7667-114">*Pattern*</span><span class="sxs-lookup"><span data-stu-id="a7667-114">*Pattern*</span></span>  <br/> |<span data-ttu-id="a7667-115">検出する部分文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7667-115">The substring to be found.</span></span>  <span data-ttu-id="a7667-116">*パターン*を空の文字列 ("") にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a7667-116">*Pattern*  cannot be an empty string ("").</span></span>  <br/> |
| <span data-ttu-id="a7667-117">*Replacement*</span><span class="sxs-lookup"><span data-stu-id="a7667-117">*Replacement*</span></span>  <br/> |<span data-ttu-id="a7667-118">置き換える文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7667-118">The replacement string.</span></span>  <br/> |
   

