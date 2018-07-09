---
title: 更新関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: 指定したフィールドの挿入または更新操作が試行されたかどうかを返します。
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798767"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="eaeb9-103">更新関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="eaeb9-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="eaeb9-104">指定したフィールドの挿入または更新操作が試行されたかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="eaeb9-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eaeb9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaeb9-107">Syntax</span></span>

 <span data-ttu-id="eaeb9-108">**更新**(*列*)</span><span class="sxs-lookup"><span data-stu-id="eaeb9-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="eaeb9-109">**更新**関数には、次の引数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="eaeb9-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="eaeb9-110">**Argument name**</span></span>|<span data-ttu-id="eaeb9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="eaeb9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eaeb9-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-112">*Column*</span></span>  <br/> |<span data-ttu-id="eaeb9-113">INSERT または UPDATE 操作をチェックするフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eaeb9-114">備考</span><span class="sxs-lookup"><span data-stu-id="eaeb9-114">Remarks</span></span>

<span data-ttu-id="eaeb9-115">**更新**関数は、挿入または更新の試行が成功したかどうかに関係なく、TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

