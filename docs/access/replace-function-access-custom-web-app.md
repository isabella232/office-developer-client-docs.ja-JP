---
title: 関数 (カスタム web アプリケーションのアクセス) を交換します。
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 93c8fc1d-e70c-4726-af2f-c6501d82e49b
description: 指定した文字列値のすべての一致箇所を別の文字列値に置換します。
ms.openlocfilehash: 09ba1f68973e9fb4ec8d860197509ec664e86376
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798728"
---
# <a name="replace-function-access-custom-web-app"></a><span data-ttu-id="b4653-103">関数 (カスタム web アプリケーションのアクセス) を交換します。</span><span class="sxs-lookup"><span data-stu-id="b4653-103">Replace Function (Access custom web app)</span></span>

<span data-ttu-id="b4653-104">指定した文字列値のすべての一致箇所を別の文字列値に置換します。</span><span class="sxs-lookup"><span data-stu-id="b4653-104">Replaces all occurrences of a specified string value with another string value.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b4653-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="b4653-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b4653-107">構文</span><span class="sxs-lookup"><span data-stu-id="b4653-107">Syntax</span></span>

 <span data-ttu-id="b4653-108">**交換**(*TextExpression*、*パターン*、*交換用*)</span><span class="sxs-lookup"><span data-stu-id="b4653-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span></span> 
  
<span data-ttu-id="b4653-109">**Replace** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b4653-109">The **Replace** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b4653-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="b4653-110">**Argument name**</span></span>|<span data-ttu-id="b4653-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b4653-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b4653-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="b4653-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="b4653-113">検索する文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4653-113">The string expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="b4653-114">*パターン*</span><span class="sxs-lookup"><span data-stu-id="b4653-114">*Pattern*</span></span>  <br/> |<span data-ttu-id="b4653-115">検索する部分文字列。</span><span class="sxs-lookup"><span data-stu-id="b4653-115">The substring to be found.</span></span>  <span data-ttu-id="b4653-116">*パターン*が空の文字列にすることはできません ("")。</span><span class="sxs-lookup"><span data-stu-id="b4653-116">*Pattern*  cannot be an empty string ("").</span></span>  <br/> |
| <span data-ttu-id="b4653-117">*Replacement*</span><span class="sxs-lookup"><span data-stu-id="b4653-117">*Replacement*</span></span>  <br/> |<span data-ttu-id="b4653-118">置き換える文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4653-118">The replacement string.</span></span>  <br/> |
   

