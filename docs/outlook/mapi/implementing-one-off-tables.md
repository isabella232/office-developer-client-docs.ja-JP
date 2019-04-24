---
title: 1回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310130"
---
# <a name="implementing-one-off-tables"></a><span data-ttu-id="b27cc-103">1回限りのテーブルの実装</span><span class="sxs-lookup"><span data-stu-id="b27cc-103">Implementing One-Off Tables</span></span>

<span data-ttu-id="b27cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b27cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b27cc-105">プロバイダーは、1つ以上の1回限りのテーブルを実装する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b27cc-105">Your provider might implement one or more one-off tables.</span></span> <span data-ttu-id="b27cc-106">1回限りのテーブルとは、受信者をコンテナーまたは送信メッセージの受信者一覧に直接作成するために使用される、1回限りのテンプレートの要約リストです。</span><span class="sxs-lookup"><span data-stu-id="b27cc-106">A one-off table is a summary list of one-off templates used to create recipients, either directly into a container or into the recipient list of an outgoing message.</span></span> <span data-ttu-id="b27cc-107">1回限りのテンプレートとは、特定の種類の住所に関連するデータを入力するために使用されるフォームユーザーのことです。</span><span class="sxs-lookup"><span data-stu-id="b27cc-107">A one-off template is a form users employ for entering data relevant to a particular type of address.</span></span> <span data-ttu-id="b27cc-108">ユーザーがテンプレートの操作を終了すると、プロバイダーは新しい受信者を作成してメッセージに追加します。</span><span class="sxs-lookup"><span data-stu-id="b27cc-108">When the user is finished working with the template, your provider creates the new recipient and adds it to the message.</span></span> <span data-ttu-id="b27cc-109">通常、各テンプレートは1つのアドレスの種類を処理します。</span><span class="sxs-lookup"><span data-stu-id="b27cc-109">Typically each template handles a single address type.</span></span> <span data-ttu-id="b27cc-110">ただし、テンプレートでは、複数の種類を処理することも、複数のテンプレートで同じ種類を処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-110">However, it is possible for a template to handle multiple types or for multiple templates to handle the same type.</span></span> 
  
<span data-ttu-id="b27cc-111">プロバイダーは、1回限りのテーブルに含まれる各テンプレートの**openentry**メソッドをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27cc-111">Your provider must support the **OpenEntry** method for each template that it includes in the one-off table.</span></span> <span data-ttu-id="b27cc-112">**openentry**の実装では、テンプレートの表示テーブルを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27cc-112">The implementation of **OpenEntry** should retrieve a display table for the template.</span></span> <span data-ttu-id="b27cc-113">MAPI では、表示テーブルを使用して、ユーザーに対してテンプレートを表示します。</span><span class="sxs-lookup"><span data-stu-id="b27cc-113">MAPI uses the display table to make the template visible to the user.</span></span> 
  
<span data-ttu-id="b27cc-114">1回限りのテーブルの行のほとんどはテンプレートを表していますが、一部の行を使用して、テンプレートを分類またはグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-114">Although most of the rows in one-off tables represent templates, some of the rows can be used to categorize, or group, templates.</span></span> <span data-ttu-id="b27cc-115">1回限りのテーブルの行がテンプレートを表しているかどうかは、 **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) 列の値で示されます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-115">Whether or not a row in a one-off table represents a template is indicated by the value of its **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) column.</span></span> <span data-ttu-id="b27cc-116">テンプレートを表す行には、PR_SELECTABLE 列が TRUE に設定されています。テンプレートを表さない行は、FALSE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="b27cc-116">Rows that represent templates have the PR_SELECTABLE column set to TRUE; rows that do not represent templates have it set to FALSE.</span></span>
  
<span data-ttu-id="b27cc-117">MAPI は、次の3種類の1回限りのテーブルを定義します。</span><span class="sxs-lookup"><span data-stu-id="b27cc-117">MAPI defines three types of one-off tables:</span></span>
  
- <span data-ttu-id="b27cc-118">個々のコンテナーがサポートするテンプレートを反映した、1回限りのテーブル</span><span class="sxs-lookup"><span data-stu-id="b27cc-118">A one-off table that reflects the templates that an individual container supports</span></span>
    
- <span data-ttu-id="b27cc-119">プロバイダーがサポートするすべてのテンプレートを反映する1回限りのテーブル</span><span class="sxs-lookup"><span data-stu-id="b27cc-119">A one-off table that reflects all of the templates that your provider supports</span></span> 
    
- <span data-ttu-id="b27cc-120">プロファイル内のすべてのプロバイダーと MAPI がサポートする一部のテンプレートを反映した、1回限りのテーブル。</span><span class="sxs-lookup"><span data-stu-id="b27cc-120">A one-off table that reflects all of the templates that all of the providers in the profile support plus some that MAPI supports</span></span>
    
<span data-ttu-id="b27cc-121">最初の2つの種類は、メッセージ上またはコンテナー内の受信者の作成をサポートするプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-121">The first two types are implemented by providers that support the creation recipients, either onto a message or into a container.</span></span> <span data-ttu-id="b27cc-122">プロバイダーでは、1回限りのテーブルに同じセットまたは別のテンプレートセットを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-122">Your provider can include the same set or a different set of templates in its one-off tables.</span></span> <span data-ttu-id="b27cc-123">この2種類の主な違いは、プロバイダーテーブルに、送信メッセージで使用できる受信者を作成するためのテンプレートを含める必要があります。また、コンテナーテーブルには、コンテナーに追加する受信者を作成するためのテンプレートを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27cc-123">The main difference between the two types is that your provider table should include templates for creating recipients that can be used on outgoing messages and your container table should include templates for creating recipients to be added to your container.</span></span> <span data-ttu-id="b27cc-124">コンテナーは、制限されたテンプレートのセットのみをサポートしますが、プロバイダーの1回限りのテーブルには、プロバイダーがサポートするすべてのテンプレートが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27cc-124">A container may only support a restricted set of templates, but the provider one-off table should include every template the provider supports.</span></span>
  
<span data-ttu-id="b27cc-125">1回限りのテーブルの3番目の種類は MAPI によって実装されています。プロバイダーは、 [imapisupport:: getoneofftable](imapisupport-getoneofftable.md)を呼び出すことによって、プロバイダーにアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="b27cc-125">The third type of one-off table is implemented by MAPI; providers gain access to it by calling [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).</span></span> <span data-ttu-id="b27cc-126">MAPI の1回限りのテーブルは、すべてのプロバイダーテーブルの和集合です。これには、プロファイル内のすべてのプロバイダーでサポートされているすべてのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b27cc-126">The MAPI one-off table is the union of all of the provider tables; it includes every template supported by every provider in the profile.</span></span> <span data-ttu-id="b27cc-127">MAPI でサポートされているテンプレートも含まれています。</span><span class="sxs-lookup"><span data-stu-id="b27cc-127">It also includes templates supported by MAPI.</span></span> <span data-ttu-id="b27cc-128">プロバイダーは、コンテナーに対して要求されたテーブルの代わりに、このテーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-128">Your provider can use this table in place of the table requested for a container.</span></span> <span data-ttu-id="b27cc-129">ただし、この表のテンプレートは、送信メッセージの受信者の作成にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="b27cc-129">However, the templates in this table can also be used for creating recipients for outgoing messages.</span></span>
  

