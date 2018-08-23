---
title: EditRecord データ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: EditRecord データ ブロックを使用して、既存のレコード内の値を変更できます。
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798565"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="7b25b-103">EditRecord データ ブロック (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="7b25b-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="7b25b-104">**EditRecord** データ ブロックを使用して、既存のレコード内の値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="7b25b-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7b25b-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="7b25b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7b25b-107">[!メモ] **EditRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b25b-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7b25b-108">設定</span><span class="sxs-lookup"><span data-stu-id="7b25b-108">Setting</span></span>

<span data-ttu-id="7b25b-109">**EditRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7b25b-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="7b25b-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="7b25b-110">**Argument**</span></span>|<span data-ttu-id="7b25b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="7b25b-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b25b-112">**エイリアス**</span><span class="sxs-lookup"><span data-stu-id="7b25b-112">**Alias**</span></span> <br/> |<span data-ttu-id="7b25b-113">編集するレコードを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="7b25b-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="7b25b-114">*別名*引数を指定しない場合、現在のレコードを編集します。</span><span class="sxs-lookup"><span data-stu-id="7b25b-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b25b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="7b25b-115">Remarks</span></span>

<span data-ttu-id="7b25b-p103">**EditRecord** ステートメントの後に、レコードの変更を確定する前に実行するコマンドのブロックを挿入できます。 **EditRecord** データ ブロックで使用できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7b25b-p103">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed. The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="7b25b-118">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="7b25b-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="7b25b-119">Comment マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="7b25b-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="7b25b-120">Group マクロ ステートメント</span><span class="sxs-lookup"><span data-stu-id="7b25b-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="7b25b-121">もし。。。そうしたら。。。マクロ ステートメントはその他</span><span class="sxs-lookup"><span data-stu-id="7b25b-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="7b25b-122">"SetField/フィールドの設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="7b25b-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="7b25b-123">"SetLocalVar/ローカル変数の設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="7b25b-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="7b25b-124">" **SetField** /フィールドの設定" アクションを使用して、編集するレコードの新しいフィールド値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b25b-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="7b25b-125">条件に基づいて操作を実行する場合は **If...Then...Else** ステートメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b25b-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="7b25b-p104">レコードの編集を取り消すには、" **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **EditRecord** データ ブロックが終了します。</span><span class="sxs-lookup"><span data-stu-id="7b25b-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="7b25b-p105">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで作成した一番新しいレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="7b25b-p105">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


