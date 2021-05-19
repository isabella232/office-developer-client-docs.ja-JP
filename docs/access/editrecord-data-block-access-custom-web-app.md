---
title: EditRecord Data Block (Access custom Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: EditRecord データ ブロックを使用して、既存のレコード内の値を変更できます。
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418345"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="2e851-103">EditRecord Data Block (Access custom Web app)</span><span class="sxs-lookup"><span data-stu-id="2e851-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="2e851-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span><span class="sxs-lookup"><span data-stu-id="2e851-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2e851-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="2e851-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2e851-107">EditRecord データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e851-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2e851-108">Setting</span><span class="sxs-lookup"><span data-stu-id="2e851-108">Setting</span></span>

<span data-ttu-id="2e851-109">**EditRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2e851-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="2e851-110">**Arg1 と Arg2 の値**</span><span class="sxs-lookup"><span data-stu-id="2e851-110">**Argument**</span></span>|<span data-ttu-id="2e851-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2e851-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e851-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="2e851-112">**Alias**</span></span> <br/> |<span data-ttu-id="2e851-113">編集するレコードを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="2e851-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="2e851-114">引数  *Alias を指定*  しない場合は、現在のレコードが編集されます。</span><span class="sxs-lookup"><span data-stu-id="2e851-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e851-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2e851-115">Remarks</span></span>

<span data-ttu-id="2e851-p103">**EditRecord** ステートメントの後に、レコードの変更を確定する前に実行するコマンドのブロックを挿入できます。**EditRecord** データ ブロックで使用できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2e851-p103">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed. The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="2e851-118">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2e851-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="2e851-119">Comment マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="2e851-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="2e851-120">Group マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="2e851-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="2e851-121">If...Then...Else マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="2e851-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="2e851-122">"SetField/フィールドの設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2e851-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="2e851-123">"SetLocalVar/ローカル変数の設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2e851-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="2e851-124">" **SetField** /フィールドの設定" アクションを使用して、編集するレコードの新しいフィールド値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e851-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="2e851-125">条件に基づいて操作を実行する場合は **If...Then...Else** ステートメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e851-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="2e851-p104">レコードの編集を取り消すには、" **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **EditRecord** データ ブロックが終了します。</span><span class="sxs-lookup"><span data-stu-id="2e851-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="2e851-p105">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで作成した一番新しいレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="2e851-p105">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


