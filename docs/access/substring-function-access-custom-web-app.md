---
title: SubString 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: 文字列式の一部が返されます。
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433473"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="4dcbf-103">SubString 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="4dcbf-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="4dcbf-104">文字列式の一部が返されます。</span><span class="sxs-lookup"><span data-stu-id="4dcbf-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4dcbf-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="4dcbf-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4dcbf-107">構文</span><span class="sxs-lookup"><span data-stu-id="4dcbf-107">Syntax</span></span>

 <span data-ttu-id="4dcbf-108">**SubString** (*TextExpression*, *Start*, *Length*)</span><span class="sxs-lookup"><span data-stu-id="4dcbf-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="4dcbf-109">**SubString** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="4dcbf-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="4dcbf-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="4dcbf-110">**Argument name**</span></span>|<span data-ttu-id="4dcbf-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4dcbf-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4dcbf-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="4dcbf-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="4dcbf-113">文字列式。</span><span class="sxs-lookup"><span data-stu-id="4dcbf-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="4dcbf-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="4dcbf-114">*Start*</span></span>  <br/> |<span data-ttu-id="4dcbf-p102">返される文字の開始位置を指定する整数式。Start が 1 未満の場合、返される式は式に指定された最初の文字から始まります。 この場合、返される文字列の数は、Start + Length - 1 または 0 のいずれか大きい方になります。開始位置が値式の文字数を超える場合は、長さゼロの式が返されます。</span><span class="sxs-lookup"><span data-stu-id="4dcbf-p102">An integer expression that specifies where the returned characters start. If start is less than 1, the returned expression will begin at the first character that is specified in expression. In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0. If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="4dcbf-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="4dcbf-119">*Length*</span></span>  <br/> |<span data-ttu-id="4dcbf-p103">返される式の文字数を指定する整数式。長さが負数の場合はエラーは生成され、ステートメントが終了します。Start と Length の合計が式の文字数を超える場合は、値式全体が先頭から返されます。</span><span class="sxs-lookup"><span data-stu-id="4dcbf-p103">A positive integer expression that specifies how many characters of the expression will be returned. If length is negative, an error is generated and the statement is terminated. If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

