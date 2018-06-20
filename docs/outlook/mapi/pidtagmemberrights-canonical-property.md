---
title: PidTagMemberRights の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2ffc6973d2670402ec8095120eea3db02f529d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802978"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="1cc24-103">PidTagMemberRights の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc24-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="1cc24-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cc24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cc24-105">フォルダーまたはメールボックスには、このメンバーの権限を指定するビットのセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1cc24-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cc24-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1cc24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cc24-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="1cc24-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="1cc24-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1cc24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cc24-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="1cc24-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="1cc24-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cc24-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1cc24-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1cc24-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1cc24-112">Area:</span></span>  <br/> |<span data-ttu-id="1cc24-113">アクセス制御</span><span class="sxs-lookup"><span data-stu-id="1cc24-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cc24-114">備考</span><span class="sxs-lookup"><span data-stu-id="1cc24-114">Remarks</span></span>

<span data-ttu-id="1cc24-115">このプロパティは、フォルダーのメンバーの権限を定義するのには、 [IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスが使用します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="1cc24-116">これらの権限を表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="1cc24-117">次の値は、このプロパティに対して定義される権限です。</span><span class="sxs-lookup"><span data-stu-id="1cc24-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="1cc24-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="1cc24-118">frightsReadAny</span></span>
  
> <span data-ttu-id="1cc24-119">メンバーは、すべてのメッセージを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-119">Member can read any messages.</span></span>
    
<span data-ttu-id="1cc24-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="1cc24-120">frightsCreate</span></span>
  
> <span data-ttu-id="1cc24-121">メンバーは、メッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-121">Member can create messages.</span></span>
    
<span data-ttu-id="1cc24-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="1cc24-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="1cc24-123">メンバーは、ユーザーが所有するすべてのメッセージを編集できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="1cc24-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="1cc24-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="1cc24-125">メンバーは、ユーザーが所有するすべてのメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="1cc24-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="1cc24-126">frightsEditAny</span></span>
  
> <span data-ttu-id="1cc24-127">メンバーは、任意のメッセージを編集できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-127">Member can edit any message.</span></span>
    
<span data-ttu-id="1cc24-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="1cc24-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="1cc24-129">メンバーは、任意のメッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-129">Member can delete any message.</span></span>
    
<span data-ttu-id="1cc24-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="1cc24-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="1cc24-131">メンバーは、フォルダーのサブフォルダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="1cc24-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="1cc24-132">frightsOwner</span></span>
  
> <span data-ttu-id="1cc24-133">メンバーは、フォルダーの以前のすべての権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="1cc24-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="1cc24-134">frightsContact</span></span>
  
> <span data-ttu-id="1cc24-135">メンバーは、フォルダーの連絡先として表示される自分の名前を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="1cc24-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="1cc24-136">frightsVisible</span></span>
  
> <span data-ttu-id="1cc24-137">メンバーは、フォルダーが存在することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="1cc24-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="1cc24-138">rightsNone</span></span>
  
> <span data-ttu-id="1cc24-139">メンバーには、フォルダーの権限がありません。</span><span class="sxs-lookup"><span data-stu-id="1cc24-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="1cc24-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1cc24-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="1cc24-141">メンバーは、フォルダー内のメッセージを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="1cc24-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1cc24-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="1cc24-143">メンバーから読み書きできるフォルダー内のメッセージにします。</span><span class="sxs-lookup"><span data-stu-id="1cc24-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="1cc24-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="1cc24-144">rightsAll</span></span>
  
> <span data-ttu-id="1cc24-145">メンバーは、フォルダーの以前のすべての権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="1cc24-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1cc24-146">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1cc24-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cc24-147">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1cc24-147">Protocol specifications</span></span>

<span data-ttu-id="1cc24-148">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc24-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc24-149">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cc24-150">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc24-150">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc24-151">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-151">Handles folder operations.</span></span>
    
<span data-ttu-id="1cc24-152">[[MS OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc24-152">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc24-153">サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="1cc24-154">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc24-154">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc24-155">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のアイテムとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cc24-156">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc24-156">Header files</span></span>

<span data-ttu-id="1cc24-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cc24-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cc24-158">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cc24-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cc24-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cc24-159">Mapitags.h</span></span>
  
> <span data-ttu-id="1cc24-160">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1cc24-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cc24-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cc24-161">See also</span></span>



[<span data-ttu-id="1cc24-162">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cc24-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="1cc24-163">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc24-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cc24-164">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc24-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cc24-165">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1cc24-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cc24-166">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1cc24-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

