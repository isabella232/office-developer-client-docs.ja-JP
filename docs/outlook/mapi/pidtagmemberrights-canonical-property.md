---
title: PidTagMemberRights 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342695"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="9d3cd-103">PidTagMemberRights 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d3cd-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="9d3cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d3cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d3cd-105">フォルダーまたはメールボックスでこのメンバーの権限を示す一連のビットを含みます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d3cd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9d3cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d3cd-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="9d3cd-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="9d3cd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9d3cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d3cd-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="9d3cd-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="9d3cd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9d3cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d3cd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9d3cd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9d3cd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9d3cd-112">Area:</span></span>  <br/> |<span data-ttu-id="9d3cd-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="9d3cd-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d3cd-114">解説</span><span class="sxs-lookup"><span data-stu-id="9d3cd-114">Remarks</span></span>

<span data-ttu-id="9d3cd-115">このプロパティは、 [IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスで、フォルダーのメンバーの権限を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="9d3cd-116">これらの権限は、表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="9d3cd-117">次の値は、このプロパティに対して定義されている権限です。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="9d3cd-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="9d3cd-118">frightsReadAny</span></span>
  
> <span data-ttu-id="9d3cd-119">メンバーは任意のメッセージを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-119">Member can read any messages.</span></span>
    
<span data-ttu-id="9d3cd-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="9d3cd-120">frightsCreate</span></span>
  
> <span data-ttu-id="9d3cd-121">メンバーはメッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-121">Member can create messages.</span></span>
    
<span data-ttu-id="9d3cd-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="9d3cd-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="9d3cd-123">メンバーは、ユーザーが所有するすべてのメッセージを編集できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="9d3cd-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="9d3cd-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="9d3cd-125">メンバーは、ユーザーが所有するすべてのメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="9d3cd-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="9d3cd-126">frightsEditAny</span></span>
  
> <span data-ttu-id="9d3cd-127">メンバーは任意のメッセージを編集できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-127">Member can edit any message.</span></span>
    
<span data-ttu-id="9d3cd-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="9d3cd-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="9d3cd-129">メンバーは任意のメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-129">Member can delete any message.</span></span>
    
<span data-ttu-id="9d3cd-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="9d3cd-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="9d3cd-131">メンバーは、フォルダーのサブフォルダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="9d3cd-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="9d3cd-132">frightsOwner</span></span>
  
> <span data-ttu-id="9d3cd-133">メンバーは、フォルダーに対する以前のすべての権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="9d3cd-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="9d3cd-134">frightsContact</span></span>
  
> <span data-ttu-id="9d3cd-135">メンバーは、フォルダーの連絡先として自分の名前を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="9d3cd-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="9d3cd-136">frightsVisible</span></span>
  
> <span data-ttu-id="9d3cd-137">メンバーはフォルダーが存在することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="9d3cd-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="9d3cd-138">rightsNone</span></span>
  
> <span data-ttu-id="9d3cd-139">メンバーにフォルダーに対する権限がありません。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="9d3cd-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="9d3cd-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="9d3cd-141">メンバーは、フォルダー内の任意のメッセージを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="9d3cd-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="9d3cd-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="9d3cd-143">メンバーは、フォルダー内のメッセージの読み取りおよび書き込みを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="9d3cd-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="9d3cd-144">rightsAll</span></span>
  
> <span data-ttu-id="9d3cd-145">メンバーは、フォルダーに対する以前のすべての権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9d3cd-146">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d3cd-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d3cd-147">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9d3cd-147">Protocol specifications</span></span>

<span data-ttu-id="9d3cd-148">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d3cd-149">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d3cd-150">[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d3cd-151">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-151">Handles folder operations.</span></span>
    
<span data-ttu-id="9d3cd-152">[[OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d3cd-153">サーバーに格納されているフォルダーのアクセス許可リストの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="9d3cd-154">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d3cd-155">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として動作するときのメッセージと予定表のアイテムの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d3cd-156">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9d3cd-156">Header files</span></span>

<span data-ttu-id="9d3cd-157">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d3cd-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d3cd-158">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d3cd-159">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9d3cd-159">Mapitags.h</span></span>
  
> <span data-ttu-id="9d3cd-160">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d3cd-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d3cd-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d3cd-161">See also</span></span>



[<span data-ttu-id="9d3cd-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d3cd-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="9d3cd-163">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9d3cd-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d3cd-164">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d3cd-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d3cd-165">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d3cd-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d3cd-166">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d3cd-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

