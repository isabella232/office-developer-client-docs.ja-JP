---
title: CreateRecord データブロック (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: CreateRecord データ ブロックを使用して、指定したテーブルに新しいレコードを作成できます。
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421376"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="46597-103">CreateRecord データブロック (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="46597-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="46597-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span><span class="sxs-lookup"><span data-stu-id="46597-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="46597-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="46597-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="46597-107">**CreateRecord** データ ブロックはデータ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="46597-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="46597-108">Setting</span><span class="sxs-lookup"><span data-stu-id="46597-108">Setting</span></span>

<span data-ttu-id="46597-109">**CreateRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="46597-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="46597-110">**CreateRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="46597-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="46597-111">**引数名**</span><span class="sxs-lookup"><span data-stu-id="46597-111">**Argument name**</span></span>|<span data-ttu-id="46597-112">**必須**</span><span class="sxs-lookup"><span data-stu-id="46597-112">**Required**</span></span>|<span data-ttu-id="46597-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="46597-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46597-114">**Create a Record In**/レコードの作成先</span><span class="sxs-lookup"><span data-stu-id="46597-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="46597-115">はい</span><span class="sxs-lookup"><span data-stu-id="46597-115">Yes</span></span>  <br/> |<span data-ttu-id="46597-116">新しいレコードを作成するテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="46597-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="46597-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="46597-117">**Alias**</span></span> <br/> |<span data-ttu-id="46597-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="46597-118">No</span></span>  <br/> |<span data-ttu-id="46597-p102">レコードを識別する文字列。レコードの別名を使用できます。</span><span class="sxs-lookup"><span data-stu-id="46597-p102">A string that identifies the record. You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46597-121">注釈</span><span class="sxs-lookup"><span data-stu-id="46597-121">Remarks</span></span>

<span data-ttu-id="46597-122">**CreateRecord** で作成したレコードは自動的にカレント レコードになります。</span><span class="sxs-lookup"><span data-stu-id="46597-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="46597-p103">**CreateRecord** ステートメントの後に、新しいレコードの作成を確定する前に実行するコマンドのブロックを挿入できます。 **CreateRecord** データ ブロックで使用できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="46597-p103">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed. The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="46597-125">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="46597-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="46597-126">Comment マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="46597-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="46597-127">Group マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="46597-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="46597-128">If...Then...Else マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="46597-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="46597-129">"SetField/フィールドの設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="46597-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="46597-130">"SetLocalVar/ローカル変数の設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="46597-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="46597-131">" **CreateRecord** /レコードの作成" アクションでレコードを作成した後、" **SetField** /フィールドの設定" アクションを使用して、新しいレコードのフィールド値を指定します。</span><span class="sxs-lookup"><span data-stu-id="46597-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="46597-132">条件に基づいて操作を実行する場合は **If...Then...Else** ステートメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="46597-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="46597-p104">レコードの作成を取り消すには " **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **CreateRecord** データ ブロックが終了します。</span><span class="sxs-lookup"><span data-stu-id="46597-p104">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="46597-p105">新しいレコードの作成を確定すると、 **LastCreateRecordIdentity** ローカル変数を使用してレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="46597-p105">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record. For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


