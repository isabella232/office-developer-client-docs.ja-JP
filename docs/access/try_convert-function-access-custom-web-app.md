---
title: Try_Convert 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: 指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798772"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="2c134-103">Try_Convert 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="2c134-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="2c134-104">指定したデータ型に値を変換します。変換が無効な場合は Null を返します。</span><span class="sxs-lookup"><span data-stu-id="2c134-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2c134-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="2c134-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2c134-107">構文</span><span class="sxs-lookup"><span data-stu-id="2c134-107">Syntax</span></span>

 <span data-ttu-id="2c134-108">**Try_Convert**(*データ型*、*式*)</span><span class="sxs-lookup"><span data-stu-id="2c134-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="2c134-109">**Try_Convert** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2c134-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2c134-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="2c134-110">**Argument name**</span></span>|<span data-ttu-id="2c134-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2c134-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2c134-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="2c134-112">*DataType*</span></span>  <br/> |<span data-ttu-id="2c134-113">*式*に変換するためにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c134-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="2c134-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="2c134-114">*Expression*</span></span>  <br/> |<span data-ttu-id="2c134-115">変換する値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c134-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c134-116">解説</span><span class="sxs-lookup"><span data-stu-id="2c134-116">Remarks</span></span>

 <span data-ttu-id="2c134-p102">**Try_Convert** は渡された値を取得し、指定された  *DataType*  への変換を試みます。変換が成功した場合、 **Try_Convert** は  *DataType*  で指定された型で値を返します。エラーが発生した場合は null が返されます。ただし、明示的に許可されていない変換を要求すると、 **Try_Convert** はエラーになって失敗します。</span><span class="sxs-lookup"><span data-stu-id="2c134-p102">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  . If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned. However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

