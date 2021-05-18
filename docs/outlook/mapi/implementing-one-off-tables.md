---
title: テーブルOne-Off実装する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421642"
---
# <a name="implementing-one-off-tables"></a><span data-ttu-id="8517c-103">テーブルOne-Off実装する</span><span class="sxs-lookup"><span data-stu-id="8517c-103">Implementing One-Off Tables</span></span>

<span data-ttu-id="8517c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8517c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8517c-105">プロバイダーは、1 つ以上の 1 回きりテーブルを実装する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8517c-105">Your provider might implement one or more one-off tables.</span></span> <span data-ttu-id="8517c-106">1 回の表は、受信者をコンテナーに直接、または送信メッセージの受信者リストに作成するために使用される 1 回きりテンプレートの概要リストです。</span><span class="sxs-lookup"><span data-stu-id="8517c-106">A one-off table is a summary list of one-off templates used to create recipients, either directly into a container or into the recipient list of an outgoing message.</span></span> <span data-ttu-id="8517c-107">1 回限定のテンプレートは、ユーザーが特定の種類のアドレスに関連するデータを入力するために使用するフォームです。</span><span class="sxs-lookup"><span data-stu-id="8517c-107">A one-off template is a form users employ for entering data relevant to a particular type of address.</span></span> <span data-ttu-id="8517c-108">ユーザーがテンプレートの操作を完了すると、プロバイダーは新しい受信者を作成し、メッセージに追加します。</span><span class="sxs-lookup"><span data-stu-id="8517c-108">When the user is finished working with the template, your provider creates the new recipient and adds it to the message.</span></span> <span data-ttu-id="8517c-109">通常、各テンプレートは 1 つのアドレスの種類を処理します。</span><span class="sxs-lookup"><span data-stu-id="8517c-109">Typically each template handles a single address type.</span></span> <span data-ttu-id="8517c-110">ただし、テンプレートで複数の型を処理したり、複数のテンプレートで同じ型を処理したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8517c-110">However, it is possible for a template to handle multiple types or for multiple templates to handle the same type.</span></span> 
  
<span data-ttu-id="8517c-111">プロバイダーは、一時テーブル **に含まれるテンプレートごとに OpenEntry** メソッドをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8517c-111">Your provider must support the **OpenEntry** method for each template that it includes in the one-off table.</span></span> <span data-ttu-id="8517c-112">**OpenEntry の実装では、** テンプレートの表示テーブルを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8517c-112">The implementation of **OpenEntry** should retrieve a display table for the template.</span></span> <span data-ttu-id="8517c-113">MAPI では、表示テーブルを使用してテンプレートをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="8517c-113">MAPI uses the display table to make the template visible to the user.</span></span> 
  
<span data-ttu-id="8517c-114">1 回表のほとんどの行はテンプレートを表しますが、一部の行を使用してテンプレートを分類またはグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="8517c-114">Although most of the rows in one-off tables represent templates, some of the rows can be used to categorize, or group, templates.</span></span> <span data-ttu-id="8517c-115">1 回表の行がテンプレートを表すかどうかは、テンプレート **(** [PidTagSelectable](pidtagselectable-canonical-property.md)) 列のPR_SELECTABLEで示されます。</span><span class="sxs-lookup"><span data-stu-id="8517c-115">Whether or not a row in a one-off table represents a template is indicated by the value of its **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) column.</span></span> <span data-ttu-id="8517c-116">テンプレートを表す行には、列PR_SELECTABLE TRUE に設定されます。テンプレートを表していない行は FALSE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="8517c-116">Rows that represent templates have the PR_SELECTABLE column set to TRUE; rows that do not represent templates have it set to FALSE.</span></span>
  
<span data-ttu-id="8517c-117">MAPI では、3 種類の 1 回きりテーブルを定義します。</span><span class="sxs-lookup"><span data-stu-id="8517c-117">MAPI defines three types of one-off tables:</span></span>
  
- <span data-ttu-id="8517c-118">個々のコンテナーがサポートするテンプレートを反映する 1 回のテーブル</span><span class="sxs-lookup"><span data-stu-id="8517c-118">A one-off table that reflects the templates that an individual container supports</span></span>
    
- <span data-ttu-id="8517c-119">プロバイダーがサポートしているすべてのテンプレートを反映する 1 回のテーブル</span><span class="sxs-lookup"><span data-stu-id="8517c-119">A one-off table that reflects all of the templates that your provider supports</span></span> 
    
- <span data-ttu-id="8517c-120">プロファイル内のすべてのプロバイダーがサポートするテンプレートと MAPI がサポートする一部のテンプレートを反映する 1 回のテーブル</span><span class="sxs-lookup"><span data-stu-id="8517c-120">A one-off table that reflects all of the templates that all of the providers in the profile support plus some that MAPI supports</span></span>
    
<span data-ttu-id="8517c-121">最初の 2 つの種類は、作成受信者をサポートするプロバイダーによって、メッセージまたはコンテナーに実装されます。</span><span class="sxs-lookup"><span data-stu-id="8517c-121">The first two types are implemented by providers that support the creation recipients, either onto a message or into a container.</span></span> <span data-ttu-id="8517c-122">プロバイダーは、同じセットまたは別のテンプレート セットを 1 回きりテーブルに含めできます。</span><span class="sxs-lookup"><span data-stu-id="8517c-122">Your provider can include the same set or a different set of templates in its one-off tables.</span></span> <span data-ttu-id="8517c-123">2 つの種類の主な違いは、プロバイダー テーブルに送信メッセージで使用できる受信者を作成するためのテンプレートを含める必要がある点と、コンテナー テーブルにコンテナーに追加する受信者を作成するためのテンプレートを含める必要がある点です。</span><span class="sxs-lookup"><span data-stu-id="8517c-123">The main difference between the two types is that your provider table should include templates for creating recipients that can be used on outgoing messages and your container table should include templates for creating recipients to be added to your container.</span></span> <span data-ttu-id="8517c-124">コンテナーは、制限された一連のテンプレートのみをサポートできますが、プロバイダーの 1 回限りテーブルには、プロバイダーがサポートしているすべてのテンプレートを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8517c-124">A container may only support a restricted set of templates, but the provider one-off table should include every template the provider supports.</span></span>
  
<span data-ttu-id="8517c-125">3 番目の種類の 1 回きりテーブルは MAPI によって実装されます。プロバイダーは [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を呼び出すことによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8517c-125">The third type of one-off table is implemented by MAPI; providers gain access to it by calling [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).</span></span> <span data-ttu-id="8517c-126">MAPI の一時テーブルは、すべてのプロバイダー テーブルの結合です。これには、プロファイル内のすべてのプロバイダーでサポートされるすべてのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8517c-126">The MAPI one-off table is the union of all of the provider tables; it includes every template supported by every provider in the profile.</span></span> <span data-ttu-id="8517c-127">また、MAPI でサポートされるテンプレートも含まれています。</span><span class="sxs-lookup"><span data-stu-id="8517c-127">It also includes templates supported by MAPI.</span></span> <span data-ttu-id="8517c-128">プロバイダーは、コンテナーに対して要求されたテーブルの代りでこのテーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8517c-128">Your provider can use this table in place of the table requested for a container.</span></span> <span data-ttu-id="8517c-129">ただし、この表のテンプレートは、送信メッセージの受信者の作成にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="8517c-129">However, the templates in this table can also be used for creating recipients for outgoing messages.</span></span>
  

