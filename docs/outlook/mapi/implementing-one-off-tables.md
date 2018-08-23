---
title: 1 回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b86ec02c0255d892c42a9be9610d31b76041822c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579110"
---
# <a name="implementing-one-off-tables"></a><span data-ttu-id="74d08-103">1 回限りのテーブルの実装</span><span class="sxs-lookup"><span data-stu-id="74d08-103">Implementing One-Off Tables</span></span>

<span data-ttu-id="74d08-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74d08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74d08-105">プロバイダーは、1 つまたは複数の一時テーブルを実装できます。</span><span class="sxs-lookup"><span data-stu-id="74d08-105">Your provider might implement one or more one-off tables.</span></span> <span data-ttu-id="74d08-106">一時テーブルは、コンテナー内に直接、または送信メッセージの受信者リストに受信者を作成するために使用 1 回限りのテンプレートの概要の一覧です。</span><span class="sxs-lookup"><span data-stu-id="74d08-106">A one-off table is a summary list of one-off templates used to create recipients, either directly into a container or into the recipient list of an outgoing message.</span></span> <span data-ttu-id="74d08-107">1 回限りのテンプレートは、アドレスの特定の種類に関連するデータを入力するフォームのユーザーの採用です。</span><span class="sxs-lookup"><span data-stu-id="74d08-107">A one-off template is a form users employ for entering data relevant to a particular type of address.</span></span> <span data-ttu-id="74d08-108">ユーザーが完了すると、テンプレートを使用する、プロバイダーは新しい受信者を作成し、メッセージに追加します。</span><span class="sxs-lookup"><span data-stu-id="74d08-108">When the user is finished working with the template, your provider creates the new recipient and adds it to the message.</span></span> <span data-ttu-id="74d08-109">通常各テンプレートは、1 つのアドレスの種類を処理します。</span><span class="sxs-lookup"><span data-stu-id="74d08-109">Typically each template handles a single address type.</span></span> <span data-ttu-id="74d08-110">ただし、複数の種類を処理するためのテンプレートまたは同じ型を処理するために複数のテンプレートの使用可能なです。</span><span class="sxs-lookup"><span data-stu-id="74d08-110">However, it is possible for a template to handle multiple types or for multiple templates to handle the same type.</span></span> 
  
<span data-ttu-id="74d08-111">プロバイダーは、1 回限りの表に含まれる各テンプレートの**OpenEntry**メソッドをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="74d08-111">Your provider must support the **OpenEntry** method for each template that it includes in the one-off table.</span></span> <span data-ttu-id="74d08-112">**OpenEntry**の実装では、テンプレートの表示テーブルを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74d08-112">The implementation of **OpenEntry** should retrieve a display table for the template.</span></span> <span data-ttu-id="74d08-113">MAPI では、表示テーブルを使用して、テンプレートをユーザーに表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="74d08-113">MAPI uses the display table to make the template visible to the user.</span></span> 
  
<span data-ttu-id="74d08-114">一時テーブル内の行のほとんどは、テンプレートを表す、分類、またはテンプレートをグループ化する行の一部を使用できます。</span><span class="sxs-lookup"><span data-stu-id="74d08-114">Although most of the rows in one-off tables represent templates, some of the rows can be used to categorize, or group, templates.</span></span> <span data-ttu-id="74d08-115">一時テーブル内の行を表すかどうか、テンプレートの**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) の列の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="74d08-115">Whether or not a row in a one-off table represents a template is indicated by the value of its **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) column.</span></span> <span data-ttu-id="74d08-116">テンプレートを表す行がある、[PR_SELECTABLE] 列が TRUE に設定テンプレートではない行には、FALSE に設定することがあります。</span><span class="sxs-lookup"><span data-stu-id="74d08-116">Rows that represent templates have the PR_SELECTABLE column set to TRUE; rows that do not represent templates have it set to FALSE.</span></span>
  
<span data-ttu-id="74d08-117">MAPI には、一時テーブルの 3 種類が定義されています。</span><span class="sxs-lookup"><span data-stu-id="74d08-117">MAPI defines three types of one-off tables:</span></span>
  
- <span data-ttu-id="74d08-118">個々 のコンテナーをサポートしているテンプレートを反映する一時テーブル</span><span class="sxs-lookup"><span data-stu-id="74d08-118">A one-off table that reflects the templates that an individual container supports</span></span>
    
- <span data-ttu-id="74d08-119">一時テーブルのすべてのプロバイダーをサポートしているテンプレートを反映します。</span><span class="sxs-lookup"><span data-stu-id="74d08-119">A one-off table that reflects all of the templates that your provider supports</span></span> 
    
- <span data-ttu-id="74d08-120">一時テーブルのすべてのすべてのプロファイル プロバイダーをサポートするいると、いくつか MAPI をサポートしているテンプレートを反映します。</span><span class="sxs-lookup"><span data-stu-id="74d08-120">A one-off table that reflects all of the templates that all of the providers in the profile support plus some that MAPI supports</span></span>
    
<span data-ttu-id="74d08-121">作成受信者、メッセージの上にまたはコンテナーのいずれかをサポートするプロバイダーによっては、最初の 2 種類が実装されています。</span><span class="sxs-lookup"><span data-stu-id="74d08-121">The first two types are implemented by providers that support the creation recipients, either onto a message or into a container.</span></span> <span data-ttu-id="74d08-122">プロバイダーは、その一時テーブルで同じまたは別のテンプレートのセットを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="74d08-122">Your provider can include the same set or a different set of templates in its one-off tables.</span></span> <span data-ttu-id="74d08-123">2 種類の主な違いは、プロバイダーのテーブルには、送信メッセージで使用できる受信者を作成するためのテンプレートを含める必要があります、そのコンテナーのテーブルには、コンテナーに追加する受信者を作成するためのテンプレートを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="74d08-123">The main difference between the two types is that your provider table should include templates for creating recipients that can be used on outgoing messages and your container table should include templates for creating recipients to be added to your container.</span></span> <span data-ttu-id="74d08-124">コンテナーが制限された一連のテンプレートをサポートするだけで、プロバイダーの一時テーブルは、プロバイダーのすべてのテンプレートを含める必要がありますをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="74d08-124">A container may only support a restricted set of templates, but the provider one-off table should include every template the provider supports.</span></span>
  
<span data-ttu-id="74d08-125">一時テーブルの 3 番目の型は、MAPI のによって実装します。プロバイダーでは、 [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を呼び出すことによってアクセスができます。</span><span class="sxs-lookup"><span data-stu-id="74d08-125">The third type of one-off table is implemented by MAPI; providers gain access to it by calling [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).</span></span> <span data-ttu-id="74d08-126">MAPI の一時テーブルでは、プロバイダーのテーブルのすべての和集合です。プロファイル内のすべてのプロバイダーでサポートされているすべてのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="74d08-126">The MAPI one-off table is the union of all of the provider tables; it includes every template supported by every provider in the profile.</span></span> <span data-ttu-id="74d08-127">MAPI がサポートされているテンプレートも含まれています。</span><span class="sxs-lookup"><span data-stu-id="74d08-127">It also includes templates supported by MAPI.</span></span> <span data-ttu-id="74d08-128">プロバイダーでは、コンテナーの要求されたテーブルではなくこのテーブルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="74d08-128">Your provider can use this table in place of the table requested for a container.</span></span> <span data-ttu-id="74d08-129">ただし、テンプレートを次の表では、送信メッセージの受信者を作成するのにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="74d08-129">However, the templates in this table can also be used for creating recipients for outgoing messages.</span></span>
  

