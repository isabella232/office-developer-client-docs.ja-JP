---
title: 関数 (カスタム web アプリケーションのアクセス) を結合します。
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: 一連の引数から Null でない最初の式を返します。
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798578"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="1190e-103">関数 (カスタム web アプリケーションのアクセス) を結合します。</span><span class="sxs-lookup"><span data-stu-id="1190e-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="1190e-104">一連の引数から Null でない最初の式を返します。</span><span class="sxs-lookup"><span data-stu-id="1190e-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1190e-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="1190e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1190e-107">構文</span><span class="sxs-lookup"><span data-stu-id="1190e-107">Syntax</span></span>

<span data-ttu-id="1190e-108">**Coalesce** (Value**, [Value**], …,[Value**])</span><span class="sxs-lookup"><span data-stu-id="1190e-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="1190e-109">**Coalesce** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1190e-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="1190e-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="1190e-110">**Argument name**</span></span>|<span data-ttu-id="1190e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="1190e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1190e-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="1190e-112">*Value*</span></span>  <br/> |<span data-ttu-id="1190e-113">式。</span><span class="sxs-lookup"><span data-stu-id="1190e-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1190e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1190e-114">Remarks</span></span>

<span data-ttu-id="1190e-115">すべての引数が NULL の場合、 **Coalesce** は NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="1190e-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1190e-116">例</span><span class="sxs-lookup"><span data-stu-id="1190e-116">Example</span></span>

<span data-ttu-id="1190e-p102">次の式をテーブルの入力規則として使用します。この式は、レコードを確定する前に、First Name、Last Name, Email、Mobile Phone、Work Phone、Home Phone、および Company の各フィールドの入力を確認します。これらのどのフィールドも空で残されている場合、 **Coalesce** 関数は NULL を返します。これは、入力規則の違反です。</span><span class="sxs-lookup"><span data-stu-id="1190e-p102">The following expression is used as the validation rule for a table. The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed. If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


