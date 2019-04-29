---
title: ユーザー関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427676"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="84724-104">ユーザー関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="84724-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="84724-p102">テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="84724-p102">Inserts a text string into another text string. It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="84724-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="84724-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="84724-109">構文</span><span class="sxs-lookup"><span data-stu-id="84724-109">Syntax</span></span>

 <span data-ttu-id="84724-110">**Stuff** (IntoTextExpression**, Start**, Length**, ThisTextExpression**)</span><span class="sxs-lookup"><span data-stu-id="84724-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="84724-111">**Stuff** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="84724-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="84724-112">**引数名**</span><span class="sxs-lookup"><span data-stu-id="84724-112">**Argument name**</span></span>|<span data-ttu-id="84724-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="84724-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="84724-114">*in-extexpression*</span><span class="sxs-lookup"><span data-stu-id="84724-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="84724-115">*ThisTextExpression*によって指定されたテキストを挿入するテキストを指定するテキスト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="84724-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="84724-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="84724-116">*Start*</span></span>  <br/> |<span data-ttu-id="84724-117">削除および挿入の開始位置を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="84724-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="84724-118">開始位置または長さが負の値の場合、null 文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="84724-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="84724-119">start が最初の inを超える\*\* 場合は、null 文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="84724-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="84724-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="84724-120">*Length*</span></span>  <br/> |<span data-ttu-id="84724-121">削除する文字数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="84724-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="84724-122">length が最初の*inの inext式*よりも長い場合、削除は最後の*in、式*の最後の文字まで行われます。</span><span class="sxs-lookup"><span data-stu-id="84724-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="84724-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="84724-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="84724-124">テキスト式 hat は、inに挿入するテキスト\*\* を指定します。</span><span class="sxs-lookup"><span data-stu-id="84724-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="84724-125">この式は、*開始*時から始まる*inserviceprovider extexpression*の長さ文字を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="84724-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84724-126">注釈</span><span class="sxs-lookup"><span data-stu-id="84724-126">Remarks</span></span>

<span data-ttu-id="84724-p107">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned. If the start position is 0, a null value is returned. If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span><span class="sxs-lookup"><span data-stu-id="84724-p107">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned. If the start position is 0, a null value is returned. If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

