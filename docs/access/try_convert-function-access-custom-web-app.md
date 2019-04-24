---
title: Try_Convert 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: 指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304228"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="72c17-103">Try_Convert 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="72c17-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="72c17-104">指定したデータ型に値を変換します。変換が無効な場合は Null を返します。</span><span class="sxs-lookup"><span data-stu-id="72c17-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="72c17-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="72c17-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="72c17-107">構文</span><span class="sxs-lookup"><span data-stu-id="72c17-107">Syntax</span></span>

 <span data-ttu-id="72c17-108">**Try_Convert** (*DataType*, *Expression*)</span><span class="sxs-lookup"><span data-stu-id="72c17-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="72c17-109">**Try_Convert** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="72c17-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="72c17-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="72c17-110">**Argument name**</span></span>|<span data-ttu-id="72c17-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="72c17-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="72c17-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="72c17-112">*DataType*</span></span>  <br/> |<span data-ttu-id="72c17-113">変換する*式*のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="72c17-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="72c17-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="72c17-114">*Expression*</span></span>  <br/> |<span data-ttu-id="72c17-115">変換する値を指定します。</span><span class="sxs-lookup"><span data-stu-id="72c17-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72c17-116">解説</span><span class="sxs-lookup"><span data-stu-id="72c17-116">Remarks</span></span>

 <span data-ttu-id="72c17-p102">**Try_Convert** は渡された値を取得し、指定された  *DataType*  への変換を試みます。変換が成功した場合、 **Try_Convert** は  *DataType*  で指定された型で値を返します。エラーが発生した場合は null が返されます。ただし、明示的に許可されていない変換を要求すると、 **Try_Convert** はエラーになって失敗します。</span><span class="sxs-lookup"><span data-stu-id="72c17-p102">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  . If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned. However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

